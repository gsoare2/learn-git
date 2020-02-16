# Aprendendo git pelo terminal 😎

### Início de tudo

Primeiro de tudo, você precisa configurar umas coisinhas de usuário no seu computador, para usar o git pelo terminal. Utilize os comandos abaixo para configurar seu nome e seu e-mail. (Isso vai para o arquivo de configurações do git, para quando for realizar outras tarefas ele reconhecer quem é você).

```bash
git config --global user.name "Fulano de Tal"
git config --global user.email "fulanodetal@exemplo.br"
```

### Próximos passos

Ótimo! Você configurou as coisas. Agora podemos fazer coisas mais interessantes.

#### Repositórios? 🤔

Os repositórios podem ser criados normalmente pela interface do github, ou gitlab ou qualquer outro gerenciador de versionamento de código que está utilizando. Mas para linkar esse repositório remoto, com o seu local há duas formas:

##### Git clone

Normalmente é o mais utilizado. Quando você cria o repositório na interface, ele te fornece um link parecido com esse: (https://github.com/fulano/calculator.git) que você consegue através dele clonar o repositório remoto localmente dessa forma:

```bash
git clone https://github.com/fulano/calculator.git
```

##### Git remote

A outra forma que linkar o repositório remoto com o local é através do `git remote`. Você pode criar o repositório normalmente na interface, e você vai na sua máquina, cria uma pasta e utiliza o seguinte comando:

```bash
git remote add origin https://github.com/fulano/calculator.git
```

Ele cuidará de criar um link remoto chamado origin com o repositório calculator (https://github.com/fulano/calculator.git). Após isso, você pode conferir pra ter certeza que criou seu link remoto com o comando:

```bash
git remote -v
```

Se a saída for parecida com isso:

```bash
origin	https://github.com/fulano/calculator (fetch)
origin	https://github.com/fulano/calculator (push)
```

Então parabéns!! 🎉🎊. Você conseguiu criar o link!!!

#### Tá! Aprendi a baixar o repositório, mas... e agora? 😒

Então, agora chegou a hora de te ensinar os comandos que fazem a mágica acontecer. E isso será amplamente utilizado por você.

##### Git add

— Esse comando tem o objetivo de adicionar arquivos.<br/>
— Ok, mas adicionar pra que?<br/>
— Ops, me perdoe. Ele serve para adicionar arquivos para serem commitados.<br/>
— Commitados? What is this?<br/>
— Um momento, mais pra frente no tutorial isso vai fazer mais sentido.<br/>

É possivel adicionar os arquivos para commit com os seguintes comandos:

```bash
git add .
git add -A
```

No fundo, no fundo esses dois comandos servem para a mesma coisa. Pode utilizar tanto um quanto o outro, mas se atente a um detalhe, esses comandos vão adiconar **TODOS** os arquivos para serem commitados. Para adiconar um arquivo específico, utilize:

```bash
git add <filename>
```

##### Git status

Esse é um comando simples, serve somente para verificar o status de quais arquivos estão para ser commitados e etc..

```bash
git status
```

##### Git commit (finalmente 😅)

Esse é um comando importante, não que os outros não sejam, mas precisa se atentar para esse. Ele tem como objetivo realizar basicamente salva as alterações que você realizou. No fluxo, seria utilizar o `git add` para adicionar os arquivos, e depois o `git commit` para salvar essas alterações, e agora o mais imporatante: **git commit** só salvar LOCALMENTE (L O C A L M E N T E) suas alterações. Tudo bem? E você pode adicionar com o seguinte comando:

```bash
git commit -m "may the fourth be with you"
```

Ah, e antes que eu esqueça de mencionar, esse **-m** é para específicar uma mensagem e sim, a mensagem é obrigatória porque é de suma importância que você explique o que fez nessas alterações que você salvando.

##### Git push

Esse é um comando muito importante também, e ele é feito logo após utilizar o `git commit` e ele serve para salvar REMOTAMENTE (R E M O T A M E N T E) suas alterações, ou seja, até o `git commit` você apenas tinha salvo para você, mas agora com o `git push`, você irá disponibilizar suas alterações no repositório remotamente para todos seus amiguinhos enxergarem.

```bash
git push origin master
```

Parametros:
**origin**: Origin é aquela parada que falamos láaaaa o começo, lembra? Ele específica o endereço do repositório.
**master**: Não tinhamos falado disso antes, mas **master** é o nome da branch que você está enviando as alterações.





