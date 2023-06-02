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
