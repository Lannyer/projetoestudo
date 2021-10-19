TERMINAL & GIT

---


TERMINAL


É o Prompt de comando do Windows. É comum utilizado terminais de terceiros, ou seja, programas de terminal com funcionalidades avançadas. O Cmder, por exemplo, já vem com o Git instalado.




- Comandos básicos de terminal


__CD__ - Usado para acessar pastas/diretórios
_Ex:_
~~~
cd c:
~~~
> Este comando leva para o diretório da unidade de armazenamento principal (C:).

Podemos ter também:
~~~
/c/users/convidado
cd d:/cursos
~~~
> partindo da pasta de usuário "convidado", entramos direto na pasta "Curso" na unidade de armazenamento (D:).

Para voltar um diretório "acima" usamos 'cd..'
_Ex:_
~~~
d:/cursos
cd ..
d:
~~~

__DIR__ - para visualizar o conteúdo de um diretório, no Windows.
> Pode ser usado, também, o comando 'tree /f' para Windows ou o comando 'ls' para iOs e Linux.

__MKDIR__ - para criar um novo diretório
_Ex:_
~~~
mkdir <nome do diretório>
~~~
> para entrar no novo diretório, basca usar o comando 'cd'

---




GIT - 01


__Branch:__ as Branchs são versões, as ramificações, do nosso projeto, sendo a "Branch Master" o projeto principal.
>_Branch, do inglês, filial, ramificação, "braço"_

__Commit:__ alterações do sistema. Envio de arquivos, edições e etc. Armazena apenas as edições feitas. 

__Comandos:__ todos os comandos do Git se iniciam com o comando git.

---


Comandos básicos do Git


__Git Init__ - para iniciar um repositório, levando em consideração TODOS os arquivos e pastas dentro do diretório.
> É criada uma pasta ".git", geralmente oculta.

__Git Status__ - mostra a situação do projeto.

__Help__ - ao adicionar o comando "help" depois de um comando, abre-se a lista de opções desse comando.
_Ex:_
~~~
git commit help
~~~

__Git Add__ - adiciona os arquivos para trabalho, fazendo que sejam localizados pelo Git quando utilizamos o comando 'git status'.
_Ex:_
~~~
git add <file>
~~~

Para adicionar todos os arquivos do diretório utiliza-se a seguinte sintaxe:
~~~
git add -A
~~~
> A letra "A" de ser maiúscula. Para ver todas as opções do comando 'git add' 

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

---
