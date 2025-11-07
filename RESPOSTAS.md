# 📝 Respostas da Atividade Prática: Git e GitHub
## 1. Introdução e Conceitos
| Pergunta | Resposta |
| :--- | :--- |
| **1. Por que o Git é considerado um sistema de controle de versão distribuído?** | O Git é distribuído porque **cada cópia** de um repositório (o clone) contém **todo o histórico do projeto**. |
| **2. Qual a diferença entre working directory, staging area e repository?** | **Working Directory:** Área de edição. **Staging Area:** Local de preparação (). **Repository:** Diretório  onde o histórico é salvo. |
| **3. Para que serve o comando `git clone`?** | Copiar um repositório Git de um local (geralmente remoto) para a sua máquina local. |
| **4. Onde estão implementados fisicamente working directory, staging area e repository?** | **Working Directory:** Estrutura de arquivos visível. **Staging Area:** Arquivo `index` dentro de `.git`. **Repository:** Diretório oculto `.git`. |
| **5. Quais os estados de um arquivo no repositório do git?** | **Untracked**, **Unmodified**, **Modified** e **Staged**. |
| **6. Explique as possíveis transições de estado de um arquivo no repositório do git?** | **Modified** `git add` **Staged**. **Staged** `git commit` **Unmodified**. |
## 2. Prática com Git Local
| Comando | Resultado/Significado |
| :--- | :--- |
| `git init` | **Mensagem:** `Initialized empty Git repository...`. **Significado:** Criou o diretório oculto `.git` (Repositório Local). |
| **1. Estado antes e depois do `git add`** | **Antes:** Untracked/Modified. **Depois:** Staged. |
| **3. Objetivo do `git commit`** | Salvar permanentemente o snapshot das alterações Staged no histórico do repositório. |
| **4. Estado após o `git commit`** | Unmodified (Não Modificado/Committed). |
## 3. Conectando ao GitHub
| Pergunta | Resposta |
| :--- | :--- |
| **1. O que significa o `-u` ou `--set-upstream`?** | Define a branch remota rastreada para a branch local, permitindo `git push` e `git pull` simplificados. |
| **2. Como verificar os remotes?** | Com o comando `git remote -v`. |
