<h1>Boas Práticas com Github - Projeto Integrador Generation</h1>

O que veremos por aqui:

1. Como criar e manipular repositórios em grupo usando github projects
2. Como todos podem trabalhar no mesmo repositório separando por branchs
3. 
4. Testes no Insomnia


<br />

<h2>👣 Passo 01 - Criar o repositório oficial do projeto integrador usando Github Projects</h2>

1. No github, criar uma nova conta **APENAS** para o projeto integrador, pois na hora que fizermos o deploy da aplicação, a conta precisará ser unicamente do projeto *para criação do projeto, usar esta documentação -> *.
<div align="left"><img src="https://i.imgur.com/JACNZiR.png" title="source: imgur.com" width="25px"/> <a href="https://github.com/rafaelq80/cookbook_spring/blob/main/04_fluxo_git/02_github_organizations.md" target="_blank"><b>Como trabalhar com github organizations</b></a></div>

2. Feito o repositório vocês precisarão se adicionar como colaboradores deste projeto, para que todos consigam ter a permissão de manipular os códigos dentro desse repositório, de acordo com o passo a passo abaixo.

Na raiz do projeto clicar em settings

<div align="center"><img src="https://i.imgur.com/cv7WKA2.png" title="source: imgur.com" width="65%"/></div>

Depois em Colaborators

<div align="center"><img src="https://i.imgur.com/fgAgNZq.png" title="source: imgur.com" width="65%"/></div>

E depois em Add People, inserindo ou o email ou o nome de usuário das pessoas do grupo do projeto integrador. *Depois do convite chequem no email de vocês para aceitar a solicitação.*

<div align="center"><img src="https://i.imgur.com/3v1NgCH.png" title="source: imgur.com" width="65%"/></div>

Feito isso, **TODOS** os integrantes do grupo precisam clonar o repositório em sua máquina, na raiz do projeto clicando em clone 

<div align="center"><img src="https://i.imgur.com/sDq3JBT.png" title="source: imgur.com" width="65%"/></div>

Selecionando o link do repositório

<div align="center"><img src="https://i.imgur.com/p5UDEb0.png" title="source: imgur.com" width="65%"/></div>

Abrindo um gitbash local em sua maquina, e usando o comando *git clone o link do repositorio do seu projeto*

<div align="center"><img src="https://i.imgur.com/FAXISIn.png" title="source: imgur.com" width="65%"/></div>

<br />

<h2>👣 Passo 02 - Importar o repositório clonado dentro do Spring Tools Suite</h2>

Para que o projeto seja criado da maneira correta, é preciso já importar a pasta clonada para o Spring Tools suite, dessa forma garantimos que estamos trabalhando no mesmo projeto, e ficará mais facil na hora de subir as alterações para o github.



<h2>👣 Passo 03 - Trabalhando, atualizando, e criando o fluxo git</h2>

Após a iniciação do projeto, recomendamos que todos trabalhem com o esquema de branches, criando uma a cada Task do projeto integrador, para que todo código seja testado antes de ser incorporado na branch principal (main).

| <img src="https://i.imgur.com/vVDBDG0.png" title="source: imgur.com" width="300px"/> | <div align="left">ALERTA DE BSM: Mantenha a Atenção aos Detalhes e a comunicação, para evitar que a sua versão do projeto esteja desatualizada, e se foi você a pessoa que ficou responsavel pelo código da task, avise aos outros colegas que tem código novo no github, para que todos tenham acesso.</div> |
| ------------------------------------------------------------ | ------------------------------------------------------------ |

1. Para subir uma nova parte de trabalho, basta abrir um gitbash na pasta clonada do projeto, inserir os comandos **git checkout -b nome-da-task** e clicar em enter. Dessa forma você garante que a parte nova do código subirá para a branch no projeto, e não para a branch principal.
2. Em seguida fazer os comandos de adição de arquivos no git, com **git add .**, **git commit -m 'mensagem de commit'**, e por ultimo **git push origin nome-da-task**.

3. Após isso, para o restante das pessoas no grupo, elas precisarão entrar na pasta clonada do projeto, abrir um gitbash, e digitar os comandos **git fetch --all** para que a branch criada pela outra pessoa seja reconhecida localmente, em seguida digitar **git checkout nome-da-task** e **git pull origin nome-da-task**. Assim todos vão conseguir testar o conteúdo da branch antes dela ser mergeada na branch principal.


| <img src="https://i.imgur.com/hOgWvSc.png" title="source: imgur.com" width="100px"/> | **ATENÇÃO:** *Não pule ou esqueça de nenhum passo acima, o git e github funcionam a partir de comandos e processos, e não seguir a risca pode gerar um conflito de informações.* |
| ------------------------------------------------------------ | :----------------------------------------------------------- |

5. Por ultimo, e somente depois de testar todo o conteúdo da branch, apenas uma pessoa precisará incorporar o código da branch nome-da-task para a branch principal, dando o comando **git checkout main** e em seguida **git pull origin nome-da-task** ou mandar um pull request, diretamente pelo repositório no github. 


<div align="left"><a href="README.md"><img src="https://i.imgur.com/XMgF3gl.png" title="source: imgur.com" width="3%"/>Voltar</a></div>