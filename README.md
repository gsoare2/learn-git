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

- Esse comando tem o objetivo de adicionar arquivos.
- Ok, mas adicionar pra que?
- Ops, me perdoe. Ele serve para adicionar arquivos para serem commitados.
- Commitados? What is this?
- Um momento, mais pra frente no tutorial isso vai fazer mais sentido.

É possivel adicionar os arquivos para commit com o 



