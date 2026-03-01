# Safe Batch Processing with REST APIs

Template de atualização em lote via API REST com foco em segurança, rastreabilidade e controle de risco.

Este projeto demonstra como executar atualizações em massa (batch processing) respeitando contratos de API, evitando sobrescritas indevidas e garantindo observabilidade da operação.

---

## 🚀 Problema que este projeto resolve

Atualizações em lote parecem simples até que envolvem:

- Centenas ou milhares de registros
- Endpoints `PUT` que substituem o recurso inteiro
- Retornos inconsistentes da API
- Campos opcionais com validação assimétrica
- Risco de sobrescrita silenciosa
- Falhas difíceis de rastrear

Este template foi construído para tratar esses riscos explicitamente.

---

## 🧠 O que este projeto demonstra

- Validação e sanitização de dados de entrada
- Normalização de payloads inconsistentes
- Diferença entre ausência e `null` em APIs REST
- Controle de taxa (rate limit)
- Tratamento estruturado de erros
- Separação entre:
  - sucessos
  - falhas (com payload salvo)
  - registros não encontrados
- Possibilidade de reprocessamento seguro

Mais do que executar um script, este projeto demonstra engenharia defensiva aplicada a operações em escala.

---

## 📦 Casos de uso reais

Este template pode ser adaptado para:

- Atualizações em massa em CRMs
- Migração de tags ou categorias
- Backfill de novos campos em bases antigas
- Correções estruturais de dados
- Saneamento de base
- Reconciliação entre sistemas
- Operações administrativas em lote

Sempre que você precisar modificar muitos registros com segurança e rastreabilidade, este padrão pode ser reutilizado.

---

## 🛠 Estrutura

- Leitura de planilha (CSV/Excel)
- Validação de e-mails
- GET por identificador
- Normalização de campos inconsistentes
- Construção segura de payload
- PUT controlado
- Logs e exportação de resultados

---

## 🔒 Princípios aplicados

- PUT é substituição, não atualização parcial
- Ausência não é equivalente a `null`
- Batch exige observabilidade
- Escala amplifica erros
- Falhas precisam ser rastreáveis

---

## 🔄 Possíveis evoluções

Este projeto pode evoluir para:

- CLI tool (usando `argparse`)
- Job agendado via cron
- Microserviço interno
- Pipeline de CI/CD para migrações controladas
- Ferramenta de data quality
- Dashboard de monitoramento de batch

---

## 🎯 Por que isso é relevante para portfólio?

Porque demonstra:

- Trabalho com APIs REST reais
- Engenharia defensiva
- Pensamento em escala
- Controle de risco
- Tratamento estruturado de erro
- Responsabilidade em produção

---

## ⚠️ Observação

Este repositório utiliza endpoints e identificadores fictícios.  
Nunca exponha tokens ou URLs reais em código público.

---

## 📚 Requisitos

- Python 3.9+
- requests
- pandas

Instalação:

```bash
pip install -r requirements.txt
