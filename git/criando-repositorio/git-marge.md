# Git marge

O comando `git merge` é usado para combinar as alterações de diferentes ramos (branches) do Git. Quando você trabalha em um projeto com várias pessoas ou desenvolve diferentes funcionalidades ao mesmo tempo, é comum criar ramos separados para cada tarefa ou recurso. O `git merge` permite que você una esses ramos, incorporando as alterações de um ramo em outro.

Aqui está uma explicação passo a passo do processo de merge:

1. Primeiro, você precisa estar no ramo de **destino**, ou seja, aquele em que deseja incorporar as alterações. Você pode verificar o ramo atual usando o comando `git branch`.

2. Em seguida, execute o comando `git merge <nome_do_ramo>` para mesclar as alterações de um ramo específico no ramo atual. Por exemplo, se você quiser mesclar as alterações do ramo chamado "`feature-branch`" no ramo atual, você executaria `git merge feature-branch`.

3. O Git tentará combinar automaticamente as alterações dos dois ramos. Em muitos casos, isso é feito automaticamente sem problemas. No entanto, em alguns casos, pode ocorrer um conflito de mesclagem, quando as alterações nos mesmos arquivos nas mesmas linhas são conflitantes.

4. Se houver um conflito, o Git pausará o processo de merge e destacará os conflitos no arquivo com marcações especiais. Você precisará abrir cada arquivo conflitante, resolver os conflitos manualmente, removendo as marcações e deixando as alterações conforme desejado.

5. Após resolver todos os conflitos, você precisará fazer o commit das alterações de mesclagem usando o comando `git commit`. O Git fornecerá uma mensagem de commit padrão, mas você pode editá-la conforme necessário.

6. Após fazer o commit, o Git concluirá a mesclagem e as alterações do ramo mesclado estarão incorporadas ao ramo de destino.`

Voltar para o [README](/README.md)
