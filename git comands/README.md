# Cheat Sheet de Comandos Git

Um guia prático e rápido com os principais comandos do Git para o dia a dia do desenvolvimento de software, divididos por fluxo de trabalho.

---

## Sumário
- [1. Iniciar e Subir Projetos](#-1-para-iniciar-e-subir-projetos-githubgitlab)
- [2. Salvar e Versionar Código](#-2-para-salvar-e-fazer-versionamento)
- [3. Consultar Histórico e Alterações](#-3-para-consultar-histórico-e-diferenças)
- [4. Trabalhar com Branches](#-4-para-trabalhar-com-branches-ramificações)
- [5. Sincronizar e Baixar Atualizações](#-5-para-sincronizar-e-baixar-atualizações)
- [6. Desfazer Alterações e Erros](#-6-para-desfazer-alterações-e-apagar-erros)

---

## 1. Para Iniciar e Subir Projetos (GitHub/GitLab)
Comandos usados para transformar uma pasta local em um repositório Git e conectá-la ao repositório remoto.

| Comando | Descrição |
| :--- | :--- |
| `git init` | Inicializa um novo repositório Git local dentro da pasta atual. |
| `git remote add origin <URL-DO-REPOSITORIO>` | Conecta seu repositório local a um repositório remoto. |
| `git remote -v` | Lista as URLs dos repositórios remotos conectados. |
| `git push -u origin main` | Envia os commits para a branch `main` remota e salva a preferência. |
| `git push` | Envia novos commits locais para o repositório remoto. |
| `git clone <URL-DO-REPOSITORIO>` | Baixa uma cópia completa de um projeto remoto para a máquina. |

---

## 2. Para Salvar e Fazer Versionamento
Comandos utilitários para registrar o progresso do desenvolvimento no histórico.

| Comando | Descrição |
| :--- | :--- |
| `git status` | Exibe o estado dos arquivos (modificados, staged ou não rastreados). |
| `git add <ARQUIVO>` | Prepara um arquivo específico para o próximo commit. |
| `git add .` | Prepara **todos** os arquivos modificados/novos para o próximo commit. |
| `git commit -m "mensagem"` | Salva a versão atual do código com uma mensagem explicativa. |
| `git commit --amend -m "nova mensagem"` | Altera a mensagem do último commit realizado. |

---

## 3. Para Consultar Histórico e Diferenças
Comandos para inspecionar alterações e conferir commits antigos.

| Comando | Descrição |
| :--- | :--- |
| `git log` | Exibe o histórico completo de commits do projeto. |
| `git log --oneline` | Exibe o histórico resumido (uma linha por commit). |
| `git diff` | Mostra as alterações feitas no código antes do `git add`. |

---

## 4. Para Trabalhar com Branches (Ramificações)
Comandos para gerenciar o desenvolvimento em ambientes isolados.

| Comando | Descrição |
| :--- | :--- |
| `git branch` | Lista todas as branches locais e destaca a atual. |
| `git branch <NOME-DA-BRANCH>` | Cria uma nova branch a partir da atual. |
| `git checkout -b <NOME-DA-BRANCH>` | Cria e altera imediatamente para a nova branch. |
| `git checkout <NOME-DA-BRANCH>` | Alterna para uma branch existente. |
| `git merge <NOME-DA-BRANCH>` | Une o código da branch especificada na branch atual. |
| `git branch -d <NOME-DA-BRANCH>` | Deleta a branch local especificada. |

---

## 5. Para Sincronizar e Baixar Atualizações
Comandos para manter o repositório local alinhado com o remoto.

| Comando | Descrição |
| :--- | :--- |
| `git fetch` | Baixa as alterações do remoto sem alterar o código local. |
| `git pull` | Baixa as alterações e atualiza o código local (`fetch` + `merge`). |

---

## 6. Para Desfazer Alterações e Apagar Erros
Comandos de restauração para corrigir equívocos.

| Comando | Descrição |
| :--- | :--- |
| `git restore <ARQUIVO>` | Descarta as alterações não salvas no arquivo informado. |
| `git restore --staged <ARQUIVO>` | Remove o arquivo da área de preparação (*staging area*). |
| `git reset --soft HEAD~1` | Desfaz o último commit, mas preserva o código alterado. |
| `git reset --hard HEAD~1` | ⚠️ Desfaz o último commit e **descarta permanentemente** as alterações. |

---

*Dica: Mantenha commits pequenos e com mensagens descritivas para facilitar o versionamento do seu software.*
