# 🧾 Processamento de Arquivos CERC – Recusas e Reprocessamento

Este projeto automatiza o **tratamento de arquivos de retorno (.ret)** da **CERC (Central de Recebíveis)** e prepara arquivos de **reprocessamento** com o mesmo layout original.  
A solução foi desenvolvida em **Python**, com foco em **automação de ETL, padronização de dados e geração de arquivos consistentes** para reenvio em processos corporativos.

---

## 📌 Sumário
- [📌 Contexto](#-contexto)
- [🚀 Funcionalidades](#-funcionalidades)
- [🧠 Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [📂 Estrutura do Projeto](#-estrutura-do-projeto)
- [⚙️ Como Usar](#️-como-usar)
- [📝 Exemplos de Saída](#-exemplos-de-saída)
- [📊 Fluxo de Processamento](#-fluxo-de-processamento)
- [📌 Próximos Passos](#-próximos-passos)
- [✍️ Autor](#️-autor)
- [📝 Licença](#-licença)

---

## 📌 Contexto

Durante o processamento diário de arquivos CERC, alguns registros podem ser **recusados** por inconsistências cadastrais ou de negócio.  
Essas recusas precisam ser analisadas e **reprocessadas com o mesmo layout original**, garantindo que o arquivo esteja pronto para nova carga no ambiente de destino.

Este projeto substitui o trabalho manual por uma automação completa em Python, capaz de processar **diversos pares de arquivos (Recebido + Retorno)** de forma rápida e padronizada 🧠⚡

---

## 🚀 Funcionalidades

✅ Leitura automática dos arquivos de **entrada (Recebido)** e **retorno (.ret)**  
✅ Identificação dinâmica do **tipo de layout (SEG001 / SEG002 / SEG007 / SEG008)**  
✅ Tratamento especial para **SEG007** (chave pelo campo *Nº Documento*)  
✅ Geração de múltiplos arquivos de saída:
- `*_RECUSADOS_ENCONTRADOS.csv` → registros localizados e validados  
- `*_MOTIVO_RECUSA.csv` → ID, situação, documento e mensagem de erro  
- `*.csv` (layout original) → pronto para reprocessamento  
✅ Validação automática do cabeçalho (garante compatibilidade com o layout original)  
✅ Exibição de resumo no terminal com contagem de registros, recusas e apólices distintas  
✅ Processamento **em lote** de múltiplos arquivos com um único comando  

---

## 🧠 Tecnologias Utilizadas

- 🐍 **Python 3.13**
- 📊 **Pandas** — manipulação e limpeza de dados
- 🧰 **Glob / OS** — varredura de diretórios
- 📄 **OpenPyXL** — integração com planilhas (quando necessário)
- ⚙️ **CSV** — formato padrão de entrada e saída

---

## 📂 Estrutura do Projeto

```bash
Corrections_Policies_Refused/
├─ 📄 Process_All.py              # Script principal
├─ 📄 README.md                   # Documentação do projeto
├─ 📄 requirements.txt            # Dependências do ambiente
├─ 📄 .gitignore                  # Itens ignorados no repositório
│
├─ 📂 exemplos/                   # Arquivos fictícios de exemplo
│   ├─ CERC-SEG001_XXXX_20251003_XXXX.csv
│   ├─ CERC-SEG001_XXXX_20251003_XXXX_ret.csv
│
├─ 📂 saida_exemplo/              # Arquivos de saída gerados pelo script
│   ├─ CERC-SEG001_XXXX_20251003_XXXX_RECUSADOS_ENCONTRADOS.csv
│   ├─ CERC-SEG001_XXXX_20251003_XXXX_ret_MOTIVO_RECUSA.csv
│   ├─ CERC-SEG001_XXXX_20251003_XXXX_ret_RECUSADOS.csv
│
└─ 📂 docs/                       # Documentação e diagramas
    └─ fluxo_processamento.png
