# miniguia-estudos-notebooklm
Projeto/atividade do Bootcamp Afya - Automação de Dados com IA

# Assunto: Git
"Este guia técnico funciona como uma folha de dicas essencial para o uso do Git, um sistema de controle
de versão distribuído amplamente utilizado. O material detalha comandos fundamentais para configurar
o ambiente, iniciar novos repositórios e gerenciar o fluxo de trabalho diário de um desenvolvedor."
_Descrição do caderno temático gerado pelo próprio modelo de linguagem do NotebookLM._

O objetivo desse caderno temático é servir como um guia auxiliar prático para quem está procurando se
aprofundar ou começar a utilizar o Git.

Através dele tenho como objetivo aprender todos os comandos básicos de Git e como usá-los de maneira eficiente para trabalhar em projetos do GitHub de maneira profissional e otimizada.

# Perguntas
## "Como faço para criar um repositório no GitHub usando o Git? Me mostre um passo a passo."
Para criar um repositório no GitHub e conectá-lo ao seu computador usando o Git, você deve seguir um processo que envolve a configuração local, a criação do repositório no site do GitHub e a sincronização entre ambos
.
Aqui está o passo a passo detalhado:
1. Configure sua Identidade
Antes de começar, você precisa configurar seu nome de usuário e e-mail no Git, pois essas informações serão associadas aos seus "commits"
. Abra o terminal (ou Git Bash) e use os comandos:
git config --global user.name "Seu Nome"
.
git config --global user.email "seuemail@exemplo.com"
.
2. Inicialize o Repositório Local
Navegue até a pasta do seu projeto no computador e transforme-a em um repositório Git
.
No terminal, digite: git init
.
Isso criará uma pasta oculta chamada .git, onde o Git armazenará todo o histórico e metadados do projeto
.
3. Adicione e Comite seus Arquivos
Agora, você precisa preparar os arquivos para o primeiro envio
.
Adicione todos os arquivos ao "staging area" (área de preparação): git add .
.
Grave a primeira versão (snapshot) dos arquivos: git commit -m "Primeiro commit"
.
4. Crie o Repositório no GitHub
Para hospedar seu código online, você deve criar o "container" no servidor do GitHub
.
Acesse github.com e faça login
.
Clique no botão "+" no topo da página e selecione "New repository"
.
Dê um nome ao seu repositório e clique em "Create repository"
.
Após a criação, o GitHub mostrará uma URL (HTTPS ou SSH). Copie essa URL
.
5. Conecte o Repositório Local ao Remoto
Agora você deve dizer ao seu Git local para onde ele deve enviar os arquivos
.
Use o comando: git remote add origin <URL_COPIADA>
.
O nome "origin" é um apelido padrão para o servidor onde seu código será armazenado
.
6. Envie (Push) os Arquivos para o GitHub
Finalmente, faça o upload dos seus commits locais para o servidor
.
Use o comando: git push -u origin master
.
O parâmetro -u faz com que o Git lembre dessa configuração, permitindo que, nas próximas vezes, você use apenas git push
.
Nota: Se você estiver usando uma versão recente do Git, o nome da branch principal pode ser main em vez de master
.
Após esses passos, seu código estará visível no GitHub e pronto para ser compartilhado ou acessado de outros computadores via git clone
.

## "Como funcionam os branches no Git?"

## "Qual é a origem do Git? Quando e por que foi criado? E por quem?"

## "Git e GitHub são a mesma coisa? Há alguma diferença entre eles?"


## Links das fontes
https://git-scm.com/cheat-sheet.pdf
https://git-scm.com/book/en/v2
https://www.researchgate.net/publication/340528902_A_Beginner's_Guide_to_Git_and_GitHub
https://web.stevens.edu/hfslwiki/images/1/1d/GIT_Tutorial.pdf
