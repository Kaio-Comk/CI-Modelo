# 🤖 CI Modelo

> Matriz e modelos reutilizáveis de workflows do GitHub Actions para pacotes Python e automação de qualidade.

---

## 📦 Conteúdo

* `tests.yml`: workflow padrão de testes contínuos, como está hoje:
  * Dispara em todo `push` e `pull_request`
  * Roda em `ubuntu-latest`
  * Matriz de Python: 3.10 e 3.12
  * Instala o pacote com `pip install -e ".[dev]"` e roda `pytest -q`
  * `GITHUB_TOKEN` só com leitura (`permissions: contents: read`) e teto de 15 minutos por job

## 🚀 Como usar

1. Copie `tests.yml` para `.github/workflows/tests.yml` no repositório de destino.
2. O pacote precisa de um extra `dev` no `pyproject.toml` com o `pytest` (ex.: `dev = ["pytest>=8"]`).
3. Se o projeto precisar de binário do sistema (ex.: `ffmpeg`), acrescente um passo `apt-get install` antes do `pip install`.

## 💡 Extensões possíveis (ainda não estão no modelo)

* Matriz com `windows-latest` e Python 3.11
* `ruff check .` antes dos testes
* Cobertura com `pytest-cov`
