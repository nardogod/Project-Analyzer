# Project Analyzer

Um script Python para analisar a estrutura de projetos React/TypeScript/JavaScript.  
Ele gera relatórios detalhados sobre arquivos, componentes React, duplicações, importações problemáticas e possíveis erros de TypeScript.

---

## Funcionalidades

- Escaneia diretórios do projeto recursivamente.
- Identifica arquivos por extensão: `.js`, `.jsx`, `.ts`, `.tsx`, `.css`, `.scss`.
- Detecta componentes React.
- Analisa importações e aponta arquivos faltantes.
- Identifica arquivos duplicados (mesmo nome em diferentes pastas).
- Detecta possíveis problemas de TypeScript, como parâmetros sem tipagem e uso de `any`.
- Gera relatórios em **JSON** e **TXT** com todas as informações.

---

## Como usar

1. Clone este repositório:

```bash
git clone https://github.com/nardogod/Project-Analyzer.git
cd Project-Analyzer

## Configurações

No início do script project_analyzer.py:

PROJECT_ROOT = '.'  # Diretório do projeto a ser analisado
IGNORE_DIRS = ['.git', '.next', 'node_modules', 'coverage', '.history']
SUPPORTED_EXTENSIONS = ['.js', '.jsx', '.ts', '.tsx', '.css', '.scss']


PROJECT_ROOT → caminho do projeto que será analisado.

IGNORE_DIRS → diretórios que serão ignorados na análise.

SUPPORTED_EXTENSIONS → extensões de arquivos que serão analisadas.

----------------------------------
Estrutura do Relatório

O relatório inclui:

Resumo: total de arquivos, componentes React, duplicações, erros de importação e arquivos com potenciais erros TypeScript.

Estrutura do projeto: quantidade de arquivos por diretório e extensão.

Componentes React: localização e quantidade.

Duplicações: arquivos com nomes repetidos em diferentes pastas.

Erros de importação: importações que não foram encontradas.

Erros TypeScript: parâmetros sem tipagem e uso de any.
