# git restore-checkout-switch

## Git checkout

O `git checkout ele não` só permite criar e alternar entre branchs, mas também permite remover arquivos.

Temos um projeto já criado com a **branch master** e precisamos inserir um novo código.Seguindo as convenções de desenvolvimento temos que criar uma nova branch para inserirmos essas alterações e posteriormente enviamos para uma análise e um possível **merge** na master.

Nesse cenário o comando `git checkout` é nosso grande aliado, com ele podemos criar branchs usando a flag `-b` dessa forma:

```bash
git checkout -b novo-codigo
```

Porém como vocês já devem saber também podemos utilizar o `git checkout` para alterar entre branch já existentes, poderíamos simplesmente usar o seguinte comando para voltarmos para a branch master do nosso projeto:

```bash
git checkout master
```

Além disso podemos utilizar o `git checkout` a nível de arquivo, e assim podemos descartar todas as alterações que fizemos em um determinado arquivo.

Assim, podemos desejar descartar todas as alterações do arquivo `index.html` do nosso projeto, e como estávamos fazendo essas alterações na nossa nova branch `novo-codigo` então precisamos alternar para ela e depois descartar as alterações, para isso podemos utilizar os dois comandos:

```bash
git checkout novo-codigo

git checkout -- index.html
```

Pronto, agora temos o arquivo `index.html` sem nenhuma modificação, igual ao estado do último commit. E ainda podemos ter outras utilizações do comando `git checkout`, vocês podem verificar na [documentação](https://git-scm.com/docs/git-checkout) todas as possibilidades.

Porém como podemos perceber o `git checkout`, faz muitas coisas, tem muitas responsabilidades e isso em um momento pode nos confundir e nos deixar pensando a respeito da utilização do comando, que é bastante semelhante para várias ações.

Devemos estar sempre atentos ao nível de escopo em que vamos utilizar o comando `git checkout`. A nível de escopo de arquivo ele tem um comportamento, a nível de **commit** tem um outro comportamento e a nível de **branch** outro comportamento.

## Git restore

O `git restore` é uma nova opção quando estamos trabalhando e precisamos restaurar algum arquivo ou o projeto por completo, e isso o `git checkout` também faz, porém o `git restore` é especificamente para trabalhar com essa parte de restauração de arquivos ou projeto ao um ponto anterior que chamamos de fonte de restauração (source).

Para restaurarmos usando o `git restore` precisamos informar o ID do primeiro commit como um valor para a flag source, que é o ponto ou fonte de restauração da seguinte maneira:

```bash
git restore --source c776f0cdefd3c6e05165feecbfe6d6a484436f16 .
```

Mas podemos parar e pensar que usando o comando `git restore` a sintaxe é mais verbosa, agora temos que passar uma flag (`--source`) indicando qual o ponto, ou seja qual o estado que desejamos voltar?

A resposta é sim, e isso é uma tendência, antes tínhamos isso não só no Git, mas em muitas outras ferramentas, essa ideia de um comando realizar diversas tarefas. Porém agora os mantenedores estão dividindo as responsabilidades e deixando os comando um pouco mais verbosos, porém semanticamente melhores de identificar cada parte do comando, bem como deixa o mesmo mais organizado e de fácil compreensão para outras pessoas.

---

## Git switch

O `git switch` surge como alternativa quando estamos trabalhando com branchs. Com o `git checkout` podemos criar novas branchs e também alternamos entre os mesmos, e com o `git switch` podemos fazer o mesmo.

Uma outra possibilidade que temos usando o `git switch` é usá-lo juntamente com o comando `git branch`, assim poderíamos criar a branch com o comando `git branch` e apenas selecionarmos o mesmo com o switch:

```bash
git branch novo-branch

git switch novo-branch
```

O switch também nos fornece um atalho bastante interessante quando precisamos selecionar a branch master, podemos simplesmente utilizar um sinal de subtração ( - ) no lugar do nome do branch:

```bash
git switch -
```

Mais um possibilidade que o switch disponibiliza é alternamos para um branch remoto, no caso um branch que nosso projeto não tenha localmente ainda, então primeiro precisamos executar o comando `git fecth` para atualizarmos as informações do projeto remoto:

```bash
git fetch
```

E logo em seguida usamos o comando com a seguinte sintaxe:

```bash
git switch -c <nome-do-branch-local> --track <remoto-origin>/<nome-do-branch-remoto>
```

Voltar para o [README](/README.md)
