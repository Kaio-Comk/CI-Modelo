# 🤖 CI Modelo

> Matriz e modelos reutilizáveis de workflows do GitHub Actions para pacotes Python e automação de qualidade.

---

## 📦 Conteúdo

* `tests.yml`: Workflow padrão de testes contínuos:
  * Matriz em sistemas operacionais (`ubuntu-latest`, `windows-latest`)
  * Versões de Python: 3.10, 3.11, 3.12
  * Linting e checagem de formatação com Ruff
  * Execução de testes unitários com Pytest e relatório de cobertura XML
