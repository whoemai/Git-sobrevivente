# Objetivo: cópia de desenvolvimento de colaboração de repositório para repositório

O comando `git clone` é usado para selecionar um **repositório existente** e criar um clone ou uma cópia dele em um **repositório local**.

O comando `git clone` cria uma cópia de um repositório **git existente**, e esse repositório pode ser **local** ou **remoto**. Além disso, essa cópia é um repositório git completo, com seu próprio histórico, gerenciamento de seus próprios arquivos e é um ambiente isolado como um todo do repositório original.

Por conveniência, a clonagem cria uma **conexão remota** apontando para o repositório original. E é essa conexão que **facilita** muito a interação com o repositório central. Você pode consultar um exemplo demonstrando o `git clone` [aqui](https://www.atlassian.com/br/git/tutorials/setting-up-a-repository)!

Com o `git clone` você também pode clonar o repositório para uma pasta específica:

```bash
git clone <repositorio> <meu-projeto-clone>
```

O repositório localizado em `repositorio` é clonado para uma pasta chamada `meu-projeto-clone`.

Você também pode configurar o `git clone` e clonar o repositório a partir de uma branch específica, diferente da original dessa forma:

```bash
git clone -branch new_feature <repositorio>
```

O exemplo acima clonaria apenas a branch `new_feature` de `repositorio`. Outras configurações de opções do `git clone` você pode consultar neste [link](https://git-scm.com/docs/git-clone).

Voltar para o [REDME](https://github.com/whoemai/Git-sobrevivente/blob/bf2fa3424c5238863c7824be6e34651d7d60802d/README.md)