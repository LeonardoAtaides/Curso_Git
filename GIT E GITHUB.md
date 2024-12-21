# GIT E GITHUB

# Branch
são as ramificações de código criadas(versão especifica) sendo possível agrega-la
na versão principal

# SSH
É um protocolo de rede criptográfica para operar serviços de rede com segurança em
uma rede não segura.

# COMANDOS 

*Cd(change Directory)* : muda o local do diretório atual, para isso utilize: 
                            cd<caminho> entre ""
        **posso copiar e colar o caminho da pasta ou digitar**

*clear* : Serve para limpar o terminal

*git init* : Serve para inicializar o git criando os arquivos necessários para inicializar repositório git 

*ls(list)* : Lista o que está dentro do diretório
Ex:
ls- al(lista arquivos ocultos)

*git status* : Mostra os branchs e os commits 

*git add* : Adiciona o arquivo, para salvamento prévio e com "." 
adiciona todos os aquivos -> git add .

*git commit* : Salva o arquivo
*git commit -m ''* : Add um comentário
*git commit -a -m ''* : da um commit em vários arquivos
*git commit nome_arquivo -m ''*: para dar commit em um arquivo só

*git rm* : É usado para remover um arquivo

*git branch -M master* : Para criar uma branch Master, ou seja é uma 
ramificação no projeto

*git remote add origin (link)* : É usado para buscar o link do repositório do GitHub

*git remote -v* : É usado para ver as origens já registradas

*git remote rm origin* : É usado para remover a origem atual para adicionar outra

# SUBINDO PARA O REPOSITÓRIO

*git push*: Envia as alterações ao GitHub

*git pull* : Puxa as informações do repositório *(quando há mudanças no repositório)*

# CLONANDO UM REPOSITÓRIO
ABRE O PROJETO E CLICA EM <CODE> E DEPOIS (SSH ou HTPPS) E COPIA O LINK, LOGO APÓS UTILIZAR UM COMANDO CHAMADO *git clone*:

Ex:
git clone<link>
**Copiando todos os arquivos do repositório para a pasta selecionada incluindo a pasta**
**para trazer apenas os arquivos usa-se:**
git@github.com:LeonardoAtaides/MyProjects.git .
                                             |-> apenas add com o espaço o ponto
