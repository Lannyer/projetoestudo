###TERMINAL, GIT, WORKFLOW & GITHUB


##TERMINAL

É o Prompt de comando do Windows. É comum utilizado terminais de terceiros, ou seja, programas de terminal com funcionalidades avançadas. O Cmder, por exemplo, já vem com o Git instalado.


**- Comandos básicos de terminal**


__cd:__ Usado para acessar pastas/diretórios.
_Ex:_
~~~
<!-- cd c: -->
~~~
> Este comando leva para o diretório da unidade de armazenamento principal (C:).
Podemos ter também:
~~~
/c/users/convidado
cd d:/cursos
~~~
> partindo da pasta de usuário "convidado", entramos direto na pasta "Curso" na unidade de armazenamento (D:).

Para voltar um diretório "acima" usamos ~cd..~.
_Ex:_
~~~
d:/cursos
cd ..
d:
~~~

__dir:__ para visualizar o conteúdo de um diretório, no Windows.
> Pode ser usado, também, o comando 'tree /f' para Windows ou o comando 'ls' para iOs e Linux.

__mkdir:__ para criar um novo diretório.
_Ex:_
~~~
mkdir <nome do diretório>
~~~
> para entrar no novo diretório, basca usar o comando 'cd'

__ls:__ ppara listar os arquivos e pastas do diretório.

---


##GIT 01 - Hello Friend!

O Git é um sistema de vercionamento de código. Com versionamento é possível encurtar e simplificar os processos de produção de código, solo ou em equipe. Para realizar o versionamento, os principais servidores são o [Git Hub](https://github.com) e o (Bitbucket)[https://bitbucket.org]. Para utilizar o Git, é necessário instalá-lo, pode-se fazer isso baixando o Git diretamente do [site](https://git-scm.com). Você pode também instalar algum terminal que já venha com o Git em conjunto, como por exemplo o (Cmder)[https://cmder.net].


__Repositório:__ é o nome dado para o projeto. É literalmente um repositório de códigos.

__Branch:__ as Branchs são versões, as ramificações, do nosso projeto, sendo a "Branch Master" o projeto principal.

__Commit:__ alterações do sistema. Envio de arquivos, edições e etc. Armazena apenas as edições feitas. 

__Comandos:__ todos os comandos do Git se iniciam com o comando git.

---

**- Configurando o Git**

O primeiro passo para configurar o Git é associar um nome de usuário e um email. Esse processo acontecerá através do comando ~git config --global user.name "Nome-de-Usuário"~ e ~git config --global user.email "email@email.com"~ para configurar o email. É comum a coonfiguração, também do editor, que é feito apartir do código ~git config --global core.editor sub~

**- Comandos básicos do Git**

__Git config:__ para configurar o Git.
~~~
 git config --global
~~~
>É comum vermos comandos com apenas um traço, que é a forma abreviada de um comando enquanto com dois traços é o comando "por extenso".
>Uma outra razão é permitir distinguir uma opção, constituída por vários caracteres, de uma sequência de opções. Se 'merged' fosse escrita com um traço seria interpretada como ~-m-e-r-g-e-d~. Um exemplo disso é o comando ~git commit -am "blabla"~ que executa o 'add' (a) e atribui uma 'mensage' (m) ao commit.
>Vários programas tem o comando 'help', que você pode acessar.
__Ex:__
~~~
nome_do_programa --help
~~~
ou
~~~
nome_do_programa -h
~~~

__git --version:__ mostra se o Git está instalado e sua versão

__git init:__ - para iniciar um repositório, levando em consideração TODOS os arquivos e pastas dentro do diretório. É criada uma pasta ".git", geralmente oculta.

__git status:__ - mostra a situação do projeto.

__help:__ - ao adicionar o comando "help" depois de um comando, abre-se a lista de opções desse comando.
_Ex:_
~~~
git commit help
~~~

__git add__ - adiciona os arquivos para trabalho, fazendo que sejam localizados pelo Git quando utilizamos o comando 'git status'.
_Ex:_
~~~
git add <file>
~~~

Para adicionar todos os arquivos do diretório utiliza-se a seguinte sintaxe:
~~~
git add -A
~~~
A letra "A" deve ser maiúscula. Para ver todas as opções do comando 'git add' 

__Git Rm__ - para excluir arquivos da branch.
_Ex:_
~~~
git rm <file>
~~~

Para forçar a deleção, também do diretório acrescentamos '--comando'
~~~
git rm --comando <file>
~~~
> Ao usar 'git rm --cached "file"', removemos do histórico de edições. para mais funcionalidades 'git rm help'.

__Git Commit__ - é oque, de fato, realiza as alterações do projeto. É de boas práticas realizar um commit junto de um comentário pertinente aos trabalhos realizados no projeto.
_Ex:_
~~~
git commit -m "Comentário relevante"
~~~
> A função '-m' é utilizada para inserir um comentário ao commit. Se for usado apenas 'git commit' é necessário escrever um comentário e outros comandos, que honestamente, não consegui executar, nem fazer funcionar. Talvez pela versão do Git, ou do Cmder, serem diferentes dos usados nas vídeo-aulas. Para mais funções do 'git commit help'.
>Utilizando o comando 'git commit -am "Comentário relevante"' adicionamos diretamente os arquivos não commitados, como se usássemos o comando 'git add -A' junto do 'git commit -m'

__Git Log__ - retorna os commits feitos, com um código hash, a branch onde o commit foi realizado, dados como autor, data, etc e a mensagem do commit. 
_Ex:_
~~~
git log
~~~
-
--


##GIT - 02


__Git Branch:__ mostra com um asterisco na branch que estamos.
> Para criação de uma nova branch usamos o comando 'git branch <nomedabranch>'. Este comando irá copiar toda a branch a partir da qual está sendo criada.

__Git Checkout:__ usado para mudar para a nova branch.
_Ex:_
~~~
git checkout <branch de destino>
~~~
> Podemos usar o _git checkout_ para retornar as alterações de um arquivo.
_Ex:_
~~~
git checkout HEAD -- <file>
~~~
> o comando _HEAD_ substitui o nome da branch atual, enquanto o duplo hífen, seguido de espaço, indica que o que vier depois será o nome de um arquivo.

__Git Diff__ - para verificar quais alterações foram feitas.
_Ex:_
~~~
git diff
~~~
> Ele irá mostrar todos as linhas que foram alteradas.
>P.s1: Ele não mostra onde foi feita a alteração, é necessário analisar e comparar para identificar as alterações.
> O _git diff_ irá mostrar TODOS os arquivos modificados.
> Para mostrar apenas os títulos dos arquivos basta usar o comando '--name-only'.
_Ex:_
~~~
git diff --name-only
~~~
> Para mostrar as alterações de um único arquivo da branch, entre os que foram alterados, basta acrescentar o nome do arquivo.
_Ex:_
~~~
git diff <file>
~~~
---

Não tem necessidade de explicar que é preciso ter uma conta em um serviço de repositório Git, como o Git Hub.

---


##GIT 03 - Criando um repositório


	1. Para criar um repositório no Git Hub é preciso:
	- Ir no canto superior direito, ao lado da foto do usuário, clicar no botão de mais e em seguida em _New repository_. Ou procurar isso em algum canto da tela.
	- Adicionar um nome para o repositório, sem letras maiúsculas e caracteres especiais, uma descrição e definir se ele será público ou privado.
	- Escolhe-se criar um arquivo README ou não. É possível acrescentar um arquivos README manualmente e enviar para o repositório.
	- Escolhe-se, também, acrescentar ou não a licença do seu projeto, casa ela exista.
	- .gitignore Lorem ipsum dolor sit amet.
	- Tendo feito estes passos, basta clicar em _Create repository_
	- Será criado uma url para o repositório.
_Ex:_
~~~ 
 https://github.com/usuario/nome-do-repositorio.git
~~~

	 2. Para criar uma conexão entre um repositório local é necessário:
	- Clicar na foto de perfil > settings > SSH and GPG keys > New SSH key
	- Em seguida criasse um título para o repositório e colamos a chave pública gerada no _Git Bach_.

	 3. Para criar as chaves públicas e privadas é necessário ter o _Git Bach_ "instalado", que nada mais é do que um terminal próprio do Git. Ao instalar o Cmder, o _Git Bach_ é instalado automaticamente. É possível entrar no site oficial do _Git_ e baixá-lo para o computador ou procurar por "Git Bach" no Google e fazer o download do arquivo. Será necessário procurar um tutorial de como instalar pq eu honestamente não faço a puta.

	4. Depois de instalar o _bach_, vá até o terminal e digite o código:
~~~
ssh-keygen -t rsa -b 4096 -C "seu@email.com"
~~~
> É necessário que seja o mesmo email usado no cadastro do Git Hub
> Insira, ou não, uma senha. Confirme a senha, caso tenha colocado uma, e em seguida dê enter.

	5. No diretório, indicado pelo terminal, procure as chaves e abra a chave pública no seu editor de códigos. Copie o código da chave pública e cole na área indicada pelo _Git Hub_.

---


**-Mais comandos Git**

__Git Remote__ - é o repositório remoto, ou seja, o repositório criado no _Git Hub_.
_Ex:_
~~~
git remote add origin https://github.com/usuario/repositorio.git
~~~
> Comumente usasse o nome _origin_ para o repositório.
> Para adicionar um repositório local em um repositório remoto
usamos o comando 'add origin <url-do-diretorio.git>'
> O comando 'remote -v' mostra as opções do repositório. Normal mente os comandos possíveis são _fetch_ e _push_.
- O comando _fetch_ traz as alterações de uma branch para o repositório. Por exemplo, se um dev está no Japão, usamos o comando _fetch_.
_Ex:_
~~~
asasdas
~~~
- Já o comando _push_ envia às alterações para o repositório remoto.
_Ex:_
~~~
git push -u origin master
~~~