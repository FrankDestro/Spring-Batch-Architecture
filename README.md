# Spring Batch — Projetos de Estudo e Referência

Repositório com implementações práticas de Spring Batch, cada pasta isolando um conceito ou cenário específico do framework. A teoria e os conceitos completos (Job, Step, Chunk, Restart, Transações, 2PC, etc.) estão em [`Spring_Batch_Guia_Revisao_V3.docx`](./Spring_Batch_Guia_Revisao_V3.docx).

Este README serve como **índice rápido**: para cada pasta, uma explicação curta do que ela implementa, útil para localizar rapidamente um exemplo e reaplicar em outro projeto.

---

## 📂 Projetos

### `Spring-Batch-Project-Tasklet`
Implementação de projeto usando **Tasklet Step** — para ações únicas e pontuais (ex: deletar arquivos, chamar API, executar script), sem processamento em blocos.

### `Spring-Batch-Tipos-Leitores-Example`
Exemplos dos diferentes tipos de **ItemReader** disponíveis no Spring Batch (leitura de arquivos, banco de dados, listas, etc.) para a fase de extração do chunk.

### `Spring-Batch-Tipos-Processadores-Example`
Exemplos dos diferentes tipos de **ItemProcessor** — transformação, validação e enriquecimento de dados dentro do chunk.

### `Spring-Batch-Tipos-Escritores-Example`
Exemplos dos diferentes tipos de **ItemWriter** — gravação dos itens processados (banco, arquivo, fila, etc.) ao final do chunk.

### `Spring-Batch-Multiples-Transactions-Example/spring-batch-transactions`
Cenário de **transação simples com múltiplos bancos** (sem XA) — JobRepository em um DataSource e dados de negócio em outro, com TransactionManager dedicado por Step.

### `Spring-Batch-Distributed-Transactions-Example/SbDistributedTransactions`
Cenário de **transação distribuída (2-Phase Commit / XA)** — commit atômico envolvendo múltiplos recursos transacionais simultaneamente (bancos, mensageria).

### `Projetos Spring Batch/migracao_dados_to_db`
Projeto de **migração de dados para banco de dados** usando Spring Batch — ETL de uma fonte externa para persistência.

### `spring-batch-em-acao`
Projeto de estudo baseado no material/livro "Spring Batch em Ação" — exemplos gerais consolidando os conceitos do framework.

---

## 📘 Documentação teórica

Toda a teoria (conceitos, arquitetura, chunk processing, restart, JobRepository, paralelismo, transações, @Qualifier, 2PC e boas práticas) está centralizada no guia:

👉 [`Spring_Batch_Guia_Revisao_V3.docx`](./Spring_Batch_Guia_Revisao_V3.docx)
