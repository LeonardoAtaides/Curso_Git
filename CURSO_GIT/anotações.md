# GIT E GITHUB

# Branch
são as ramificações de código criadas(versão especifica) sendo possível agrega-la
na versão principal

*DEVE SEMPRE CRIAR BRANCHES APARTIR DA MAIN*

## Criando uma Branch
Para criar uma Branch no projeto utiliza-se, git branch <nome>

## Ver Branchs Criados
Para visualizar todos os branchs já criados no projeto utiliza-se, git branch

## Mudando de Branch
Para mudar para outro branch utiliza-se, git checkout<nome>
Para mudar e criar um novo branch utiliza-se, git checkout -b <nome>

*DEVE COMITAR ANTES DE ALTERAR DE BRANCH SE NÃO A ALTERAÇÃO VAI PARA A BRANCH ERRADA*

## Unindo Branches
Para unir branches distintos, utiliza-se, git merge <nome>

## Enviando Branches Ao Repositório
Para enviar uma branch ao repositório usa-se o comando:
git push --set-upstream origin (nome do Branch)

## Deletar Branches
Para deletar um branch usa-se a flag -f ou --delete, geralmente se usa quando o branch foi criado errado
*Não é comum deletar um branch, normalmente guardamos o histórico do trabalho*
Ex: git branch -d primeiro_branch*

## Encontrando Branchs
Para encontrar uma branch já criada, para trazê-la até outro ponto de desenvolvimento, usa-se o comando: git fetch , onde mostrará:
[new branch]      Nome_Branch -> origin/Nome_Branch
    *ONDE PARA ACESSÁ-LO DEVE USAR GIT CHECKOUT*

## Exibindo Diferenças de um Branch
Serve para exibir as diferenças de um branch, utilizando o comando *git diff* 

**Pode-se verificar a diferença entre arquivos: *git diff <arquivo> <arquivo_2>***
Ex: Para comparar o arquivo atual com o do repositório, usa: 
*git diff HEAD:arquivo.txt arquivo.txt*

# SSH
É um protocolo de rede criptográfica para operar serviços de rede com segurança em
uma rede não segura.

# COMANDOS 

Cd(change Directory) : muda o local do diretório atual, para isso utilize: 
                            cd<caminho> entre ""
        *posso copiar e colar o caminho da pasta ou digitar*

clear : Serve para limpar o terminal

ls(list) : Lista o que está dentro do diretório
Ex:
ls- al(lista arquivos ocultos)

# INICIANDO UM REPOSITÓRIO
git init : Serve para inicializar o git criando os arquivos necessários para inicializar repositório git 

# BUSCANDO REPOSITÓRIO
git branch -M master : Para criar uma branch Master, ou seja é uma 
ramificação no projeto

git remote add origin (link) : É usado para buscar o link do repositório do GitHub

git remote -v : É usado para ver as origens já registradas

git remote rm origin : É usado para remover a origem atual para adicionar outra

# VERIFICAR STATUS DO REPOSITÓRIO
git status : Mostra os branchs e os commits 

# ADICIONAR ARQUIVOS
git add : Adiciona o arquivo, para salvamento prévio e com "." 
adiciona todos os aquivos -> git add .

# COMITAR ARQUIVOS
git commit : Salva o arquivo
git commit -m '' : Add um comentário
git commit -a -m '' : da um commit em vários arquivos
git commit nome_arquivo -m '': para dar commit em um arquivo só

# SUBINDO PARA O REPOSITÓRIO    
git push: Envia as alterações ao GitHub

git pull : Puxa as informações do repositório (quando há mudanças no repositório)

# CLONANDO UM REPOSITÓRIO
ABRE O PROJETO E CLICA EM <CODE> E DEPOIS (SSH ou HTPPS) E COPIA O LINK, LOGO APÓS UTILIZAR UM COMANDO CHAMADO git clone:

Ex:
git clone<link>
*Copiando todos os arquivos do repositório para a pasta selecionada incluindo a pasta*
*para trazer apenas os arquivos usa-se:*
git@github.com:LeonardoAtaides/MyProjects.git .
                                             |-> apenas add com o espaço o ponto

# REMOVER ARQUIVOS DO REPOSITÓRIO
Remove arquivos, não só deletando do GitHub mais também do projeto alocado da máquina local (PC)

git rm -f (nome_arq) : É usado para remover um arquivo após ter dado um add

git rm (nome_arq) : É usado para remover um arquivo após ter dado um commit
**Onde não precisa adicionar o arquivo usando git add apenas sendo necessário dar commit**

# HISTÓRICO DE ALTERAÇÕES
Possibilita acessar as modificações feitas no projeto, utilizando: git log
**recebendo informações sobre os commits já realizados no projeto**
                                                ______Mostrando:_______
commit 6eb1549e5be7553cbb                      |    Código do Commit    |
Author: Leonardo Ataídes <leonardo@gmail.com>  | Nome e Email da pessoa |
Date:  Sun Dec 29 17:39:38 2024                |     Data Mês e Hora    |
    delete file                                |   Mensagem do Commit   |
                                               ||
         **Apertando ENTER vai mostrando todas as alterações**
         
## Log Resumido
Mostra um Histórico de alterações de forma resumida, utilizando: *git shortlog*


# RENOMEAR ARQUIVOS
Possibilita renomear e mover arquivos dentro do projeto, utilizando: *git mv*
movendo : git mv (arquivo) (pasta)/(arquivo)

renomeado : git mv (pasta)/(arquivo) (pasta)/(novo nome do arquivo)

# DESFAZENDO ALTERAÇÕES "MOMENTÂNEAS"
O arquivo modificado retorna ao estado original, utilizando: *git checkout*

Ex: Realiza-se uma modificação e decide apagar, mesmo apagando o git identifica uma alteração,
então usa git checkout (arquivo) para retornar ao estado original.

# DESFAZENDO TODAS AS ALTERAÇÕES
Exclui todas alterações já feitas, inclusive as comitadas, mas quando não foi enviado ao repositório ainda
utilizando git reset, geralmente é utilizado com flag --hard e a origem
Ex :git reset --hard origin/main

# IGNORANDO ARQUIVOS NO PROJETO
Usado para ignorar arquivos que não tem a necessidade de estar no repositório
utilizando: .gitinore, cria um arquivo com este nome e coloca os arquivos os nomes dos
arquivos que deseja ignorar
*É necessário adicionar o nome do arquivo no *gitignore antes de incluir o arquivo no projeto**
            *O ARQUIVO ADD EM .GITIGONE DEIXA DE SER "SUPERVISIOANDO"*

# SALVAR O CÓDIGO EM UMA "LIXEIRA"

## "CRIANDO"
Usado para salvar as modificações que talvez não serão usadas no projeto, como uma espécie de lixeira, exclui o código mais tem como recuperar depois, utiliza-se o comando git stash
após utilizar o comando o branch será resetado para a versão de acordo com o repositório
            *O COMANDO SO FUNCIONA ANTES DE DAR COMMIT*

## "VERIFICAR"
Pode-se verificar as stashs criadas pelo comando *git stash list*

## "RECUPERANDO"
Para recuperar a stash utiliza-se o comando *git stash apply (indice)*

## "VER AS MODIFICAÇÕES"
Para ver as modificações feitas no stash utiliza-se o comando *git stash show -p(indice)*

## "REMOVENDO"
Para limpar totalmaente as stash de um branch podemos utilizar o comando git stash clear
Para remover uma especifica utiliza o comando *git stash drop (indice)

# TAGS
Usada como um checkpoint de um branch, usada para demarcar estágios do desenvolvimento de algum recurso    *precisa commitar é depois salvar a TAG*

## CRIANDO A TAG
Pode-se criar tags nos branches por meio do comando git tag -a (nome) -m "(mensagem)", a tag serve como uam espécie de checkpoint, demarcando pontos do desenvolvimento do projeto

## VENDO A TAG
Para visualizar as tags já criadas utiliza-se o comando git tag

## VERIFICANDO A TAG
Podemos verificar uma tag com o comando git show (nome)
**pode ser usado para ver detalhes de um commit em branches**

## TROCAR DE TAG
Podemos trocar de tags com o comando git checkout (nome)

## ENVIAR A TAG AO REPOSITÓRIO
Podemos enviar as tags para o repositório de código, utiliza-se 
o comando git push origin(nome), para enviar todas as tags usa-se,git push origin --tags

# SUBMÓDULO
É a maneira de ter dois ou mais projetos em um só repositório. Para isso e é necessário
ter outro repositório para conciliar com o atual

## CRIANDO UM SUBMÓDULO
utiliza-se o comando - *git submodule add <link_do_repositório> submodulo*

## ATUALIZANDO O SUBMÓDULO
utiliza-se o comando - *git push --recurse-submodules=on-demand*, onde fará atualização
apenas do submódulo
