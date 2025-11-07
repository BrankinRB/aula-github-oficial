# Respostas da Atividade Prática: Git e GitHub

## 1. Introdução e Conceitos

| Pergunta | Resposta |
| :--- | :--- |
| **1. [cite_start]Por que o Git é considerado um sistema de controle de versão distribuído?** [cite: 12] | [cite_start]O Git é distribuído porque **cada cópia** de um repositório [cite: 10] [cite_start]contém **todo o histórico do projeto**, permitindo trabalho offline e controle total de versões. [cite: 10] |
| **2. [cite_start]Qual a diferença entre working directory, staging area e repository?** [cite: 14] | **Working Directory:** Área de edição e visualização dos arquivos. **Staging Area:** O local intermediário (índice) que "prepara" as alterações para o *commit*. **Repository:** O diretório `.git` onde o histórico é salvo. |
| **3. [cite_start]Para que serve o comando `git clone`?** [cite: 15] | Serve para **copiar** um repositório Git de um local (geralmente remoto) para a sua máquina local, obtendo todo o histórico do projeto. |
| **4. [cite_start]Onde estão implementados fisicamente working directory, staging area e repository?** [cite: 16] | **Working Directory:** Estrutura de arquivos visível. **Staging Area:** O arquivo `index` dentro do diretório `.git`. **Repository:** O diretório oculto `.git`. |
| **5. [cite_start]Quais os estados de um arquivo no repositório do git?** [cite: 17] | **Untracked**, **Unmodified** (Committed), **Modified** e **Staged**. |
| **6. [cite_start]Explique as possíveis transições de estado de um arquivo no repositório do git?** [cite: 18] | **Modified** $\xrightarrow{git\ add}$ **Staged**. **Staged** $\xrightarrow{git\ commit}$ **Unmodified**. **Untracked** $\xrightarrow{git\ add}$ **Staged**. |

## 2. Prática com Git Local

| Comando | Resultado/Significado |
| :--- | :--- |
| [cite_start]**`git init`** [cite: 24] | **Mensagem:** `Initialized empty Git repository...`. [cite_start]**Significado:** Criou o diretório oculto **`.git`** [cite: 16] (o Repositório Local), tornando a pasta pronta para ser monitorada. |

[cite_start]**Etapa 2 - Adicionar arquivo e fazer commit** [cite: 27]

1.  [cite_start]**Qual o estado do arquivo antes e depois do `git add`?** [cite: 33]
    * **Antes do `git add`:** **Untracked** ou **Modified**.
    * **Depois do `git add`:** **Staged** (Preparado).
2.  [cite_start]**O que significa o estado `untracked` e `tracked`?** [cite: 34]
    * **Untracked:** O Git não conhece e não está monitorando o arquivo.
    * **Tracked:** O arquivo já foi incluído em pelo menos um *commit* e é monitorado pelo Git.
3.  [cite_start]**Qual o objetivo do `git commit`?** [cite: 35]
    * Salvar permanentemente o *snapshot* das alterações que estão na **Staging Area** no histórico do repositório.
4.  [cite_start]**Qual o estado do arquivo após o `git commit`?** [cite: 36]
    * **Unmodified** (Não Modificado/Committed).

[cite_start]**Etapa 3 - Histórico e alterações** [cite: 38]

1.  [cite_start]**O que o comando `git diff` mostra?** [cite: 43]
    * Mostra as **diferenças** entre os arquivos no **Working Directory** e a última versão *commitada*.
2.  [cite_start]**Qual commit está atualmente apontado por `HEAD`?** [cite: 44]
    * O `HEAD` aponta para o **último *commit*** da *branch* atual (neste caso, o *commit* com a mensagem "Primeiro commit", assumindo a execução correta da Etapa 2).

[cite_start]**Etapa 4 - Trabalhando com Branches** [cite: 45]

1.  [cite_start]**Como verificar em qual branch você está?** [cite: 52]
    * Usando o comando **`git branch`** (que lista e marca a *branch* atual) ou **`git status`**.
2.  [cite_start]**O que acontece se você rodar `git merge nova-feature` estando na branch principal?** [cite: 53]
    * O Git irá **integrar** todas as alterações (*commits*) da *branch* `nova-feature` para a *branch* principal, unindo os históricos e, possivelmente, criando um *commit* de *merge*.

## 3. Conectando ao GitHub

1.  [cite_start]**O que significa o `-u` ou `--set-upstream` no comando `git push -u origin main`?** [cite: 62]
    * Define a *branch* remota rastreada para a *branch* local, permitindo o uso de comandos simplificados como `git push` e `git pull` a partir de então.
2.  [cite_start]**Como verificar os remotes configurados no repositório?** [cite: 63]
    * Com o comando **`git remote -v`**.

## [cite_start]4. Encerramento e Discussão [cite: 64]

* [cite_start]**Como o Git ajuda na colaboração?** [cite: 66]
    * Permite trabalho paralelo usando *branches*; mantém um histórico de alterações claro; e facilita a revisão de código (*pull requests*).
* [cite_start]**Que diferença faz ter um repositório remoto?** [cite: 67]
    * Fornece **backup** do código; cria um **ponto central** para compartilhamento e sincronização da equipe; e permite acesso distribuído ao projeto.
