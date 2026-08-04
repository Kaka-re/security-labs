# Lab 01 - Inventário de Ativos e Classificação de Criticidade

## 🎯 Objetivo
Modelar um inventário de ativos de TI (servidores, aplicações, bancos de dados, 
endpoints) e classificar sua criticidade com base na tríade CIA:
- **Confidencialidade** — quão sensível é a informação que o ativo processa/armazena
- **Integridade** — qual o impacto se os dados forem alterados indevidamente
- **Disponibilidade** — qual o impacto se o ativo ficar indisponível

## 📌 Por que isso importa
Toda análise de risco começa sabendo **o que você precisa proteger** e 
**o quão crítico é cada ativo**. Sem inventário, não existe gestão de risco — 
é o primeiro passo de frameworks como NIST SP 800-30 e ISO/IEC 27005.

## 🧩 O que este lab vai conter
- `schema.sql` — estrutura da tabela de ativos
- `seed_data.sql` — dados de exemplo (ativos fictícios de uma empresa simulada)
- `queries.sql` — consultas de priorização por criticidade
- `notas.md` — anotações sobre a metodologia usada

## 🗂️ Modelo de dados (prévia)

| Campo | Descrição |
|---|---|
| `id` | Identificador do ativo |
| `nome` | Nome do ativo (ex: "Servidor de Banco de Dados - Produção") |
| `tipo` | Servidor, Aplicação, Banco de Dados, Endpoint, etc. |
| `confidencialidade` | Nota de 1 (baixa) a 5 (alta) |
| `integridade` | Nota de 1 a 5 |
| `disponibilidade` | Nota de 1 a 5 |
| `criticidade_total` | Soma ou média ponderada das notas acima |
| `responsavel` | Área ou pessoa responsável pelo ativo |

## ✅ Checklist do lab
- [ ] Criar `schema.sql` com a tabela de ativos
- [ ] Popular com pelo menos 10 ativos fictícios variados
- [ ] Criar query que ordena ativos por criticidade (maior risco primeiro)
- [ ] Documentar a metodologia de pontuação em `notas.md`

## 📚 Referências
- NIST SP 800-30 — Guide for Conducting Risk Assessments
- ISO/IEC 27005 — Information Security Risk Management
