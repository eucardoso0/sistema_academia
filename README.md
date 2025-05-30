# sistema_academia
# 🏋️‍♀️ Sistema de Academia — Projeto de Arquitetura de Dados

Este projeto simula a construção de um sistema de gestão de academia utilizando banco de dados relacional, Python para extração e integração, e Power BI para visualização analítica.

---

## 📌 Etapas do Projeto

### 1. 📦 Modelagem e Criação do Banco de Dados
- Banco de dados `sistema_academia` criado no **MySQL**
- Tabelas: `Alunos`, `Instrutores`, `Planos`, `Matriculas`, `Pagamentos`, `Presencas`
- `id_*` com `AUTO_INCREMENT`, e chaves estrangeiras bem definidas

### 2. 🔗 Conexão com Python e Exportação (ETL)
- Uso de `mysql.connector` e `pandas` para extrair os dados e exportar para `.csv`
- Arquivo principal: [`scripts/sistema.py`](./scripts/sistema.py)
- Também foi gerada uma versão consolidada via `JOIN` entre as tabelas:
  - Resultado: [`analise/dados_academia_completo_1.csv`](./analise/dados_academia_completo_1.csv)

### 3. 🧹 Limpeza e Tratamento dos Dados
- Feita diretamente no Power BI:
  - Remoção de valores nulos
  - Remoção de duplicatas
  - Correção de formatos de data

### 4. 📊 Visualizações no Power BI
> Análises e dashboards interativos criados com os dados tratados

**Exemplos de análises feitas:**
- Presenças por mês (linha do tempo)
- Receita total por plano
- Distribuição de alunos por sexo
- Alunos inadimplentes (sem pagamento)
- Total de matrículas por plano

<ins>⚠️ Obs.:</ins> Para o gráfico de presenças por mês funcionar corretamente, as datas foram redistribuídas entre janeiro e maio de 2024 no arquivo `Presencas_Distribuidas.csv`.

---

## 🧰 Tecnologias Utilizadas

- **MySQL** — Modelagem relacional
- **Python** — Extração dos dados (`pandas`, `mysql.connector`)
- **Power BI** — Visualização dos dados
- **Git & GitHub** — Documentação e versionamento

---

## 🧠 Considerações Finais

Esse projeto demonstra um fluxo completo de arquitetura de dados:
- Da modelagem à carga e visualização
- Trabalhando com dados sujos e relacionamentos reais
- Excelente base para projetos maiores de BI e Engenharia de Dados

---

### 📎 Licença

Este projeto é livre para fins educacionais.

