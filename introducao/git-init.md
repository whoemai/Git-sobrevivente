# Inicializando um novo repositório: git init

Para criar um novo repositório, você vai usar o comando `git init`. git init é um comando único que você usa durante a configuração inicial de um novo repositório. A execução desse comando cria um novo subdiretório .git no diretório de trabalho atual. Essa ação também vai criar uma ramificação principal.

A maioria dos outros comandos Git não está disponível fora de um repositório inicializado, portanto, este costuma ser o primeiro comando que você executa em um novo projeto.

Se você já executou o `git init` em um diretório de projeto e ele contém um subdiretório .git, você pode executar outra vez o `git init` com segurança no mesmo diretório de projeto. Essa ação não vai substituir a configuração do `.git`.

## git init versus. git clone

Uma rápida observação: é fácil confundir o `git init` e o `git clone`. No nível superficial, ambos podem ser usados para "inicializar um novo repositório do Git". Contudo, o `git clone` é dependente do `git init`. O `git clone` é usado para criar uma cópia de um repositório existente. No nível interno, o `git clone` primeiro chama o `git init` para criar um novo repositório. Em seguida, copia os dados do repositório existente e faz checkout de um novo conjunto de arquivos de trabalho.

para informações mais detalhas acesse [aqui](https://www.atlassian.com/br/git/tutorials/setting-up-a-repository/git-init)

Voltar para o [REDME](https://github.com/whoemai/Git-sobrevivente/blob/bf2fa3424c5238863c7824be6e34651d7d60802d/README.md)
