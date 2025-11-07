# Respostas da Atividade Prática: Git e GitHub

## 1. Introdução e Conceitos

| Pergunta | Resposta |
| :--- | :--- |
| **1. Por que o Git é considerado um sistema de controle de versão distribuído?** | O Git é distribuído porque **cada cópia** de um repositório contém **todo o histórico do projeto**, permitindo trabalho offline e controle total de versões. |
| **2. Qual a diferença entre working directory, staging area e repository?** | **Working Directory:** Área de edição e visualização dos arquivos. **Staging Area:** O local intermediário (índice) que "prepara" as alterações para o *commit*. **Repository:** O diretório `.git` onde o histórico é salvo. |
| **3. Para que serve o comando `git clone`?** | Serve para **copiar** um repositório Git de um local (geralmente remoto) para a sua máquina local, obtendo todo o histórico do projeto. |
| **4. Onde estão implementados fisicamente working directory, staging area e repository?** | **Working Directory:** Estrutura de arquivos e pastas visível. **Staging Area:** O arquivo `index` dentro do diretório oculto `.git`. **Repository:** O diretório oculto **`.git`**. |
| **5. Quais os estados de um arquivo no repositório do git?** | **Untracked**, **Unmodified** (Committed), **Modified** e **Staged**. |
| **6. Explique as possíveis transições de estado de um arquivo no repositório do git?** | **Modified** $\xrightarrow{git\ add}$ **Staged**. **Staged** $\xrightarrow{git\ commit}$ **Unmodified**. **Untracked** $\xrightarrow{git\ add}$ **Staged**. |

## 2. Prática com Git Local

### Etapa 1 - Criar o repositório

| Comando | Resultado/Significado |
| :--- | :--- |
| **`git init`** | **Mensagem:** `Initialized empty Git repository...`. **Significado:** Criou o diretório oculto **`.git`** (o Repositório Local), tornando a pasta pronta para ser monitorada pelo Git. |

### Etapa 2 - Adicionar arquivo e fazer commit

1.  **Qual o estado do arquivo antes e depois do `git add`?**
    * **Antes do `git add`:** **Untracked** (se for um arquivo novo) ou **Modified**.
    * **Depois do `git add`:** **Staged** (Preparado).
2.  **O que significa o estado `untracked` e `tracked`?**
    * **Untracked:** O Git não conhece e não está monitorando o arquivo.
    * **Tracked:** O arquivo já foi incluído em pelo menos um *commit* e é monitorado pelo Git.
3.  **Qual o objetivo do `git commit`?**
    * Salvar permanentemente o *snapshot* das alterações que estão na **Staging Area** no histórico do repositório.
4.  **Qual o estado do arquivo após o `git commit`?**
    * **Unmodified** (Não Modificado/Committed).

### Etapa 3 - Histórico e alterações

1.  **O que o comando `git diff` mostra?**
    * Mostra as **diferenças** entre os arquivos no **Working Directory** e a última versão *commitada*.
2.  **Qual commit está atualmente apontado por `HEAD`?**
    * O `HEAD` aponta para o **último *commit*** da *branch* atual (o *commit* de mensagem "Primeiro commit", assumindo a execução correta da Etapa 2).

### Etapa 4 - Trabalhando com Branches

1.  **Como verificar em qual branch você está?**
    * Usando o comando **`git branch`** (que lista e marca a *branch* atual) ou **`git status`**.
2.  **O que acontece se você rodar `git merge nova-feature` estando na branch principal?**
    * O Git irá **integrar** todas as alterações (*commits*) da *branch* `nova-feature` para a *branch* principal, unindo os históricos e, possivelmente, criando um *commit* de *merge*.

## 3. Conectando ao GitHub

1.  **O que significa o `-u` ou `--set-upstream` no comando `git push -u origin main`?**
    * Define a *branch* remota rastreada para a *branch* local, permitindo o uso de comandos simplificados como `git push` e `git pull` a partir de então.
2.  **Como verificar os remotes configurados no repositório?**
    * Com o comando **`git remote -v`**.

## 4. Encerramento e Discussão

* **Como o Git ajuda na colaboração?**
    * Permite trabalho paralelo usando *branches*; mantém um histórico de alterações claro; e facilita a revisão de código (*pull requests*).
* **Que diferença faz ter um repositório remoto?**
    * Fornece **backup** do código; cria um **ponto central** para compartilhamento e sincronização da equipe; e permite acesso distribuído ao projeto.
