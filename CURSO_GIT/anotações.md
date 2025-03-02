# GIT

# SSH
É um protocolo de rede criptográfica para operar serviços de rede com segurança em uma rede não segura, onde pode ser copiada esse link atráves do GitHub onde possibilita ter a acesso ao repositório remoto


# Branch
são as ramificações de código criadas(versão especifica) sendo possível agrega-la na versão principal
**DEVE SEMPRE CRIAR BRANCHES APARTIR DA MAINㅤ**

## Criando uma Branch
Para criar uma Branch no projeto utiliza-se,  git checkout -b <nome>

## Ver Branchs Criados
Para visualizar todos os branchs já criados no projeto utiliza-se, *git branch*

## Mudando de Branch
Para mudar para outro branch utiliza-se, *git checkout<nome>*
**ㅤDEVE SEMPRE COMITAR ANTES DE ALTERAR DE BRANCH SE NÃO A ALTERAÇÃO VAI PARA A BRANCH ERRADAㅤ**

## Unindo Branches
Para unir branches distintos, utiliza-se: *git merge <nome>*

## Enviando Branches Ao Repositório
Para enviar uma branch ao repositório usa-se o comando:
*git push --set-upstream origin (nome do Branch)*

## Deletar Branches
Para deletar um branch usa-se a flag -f ou --delete, geralmente se usa quando o branch foi criado errado
*Não é comum deletar um branch, normalmente guardamos o histórico do trabalho*
Ex: git branch -d primeiro_branch*

## Encontrando Branchs
Para encontrar uma branch já criada, para trazê-la até outro ponto de desenvolvimento, usa-se o comando: *git fetch* , onde mostrará:
[new branch]      Nome_Branch -> origin/Nome_Branch
    *ONDE PARA ACESSÁ-LO DEVE USAR GIT CHECKOUT*

## Exibindo Diferenças de um Branch
Serve para exibir as diferenças de um branch, utilizando o comando *git diff* 

**Pode-se verificar a diferença entre arquivos: *git diff <arquivo> <arquivo_2>***
Ex: Para comparar o arquivo atual com o do repositório, usa: 
*git diff HEAD:arquivo.txt arquivo.txt*
<-------------------------------------------------------------------------------------------->


# COMANDOS BÁSICOS WINDOWS

## Cd(change Directory)
muda o local do diretório atual, utilizando: *cd<caminho>* entre ""
        **ㅤPOSSO COPIAR E COLAR O CAMINHO DA PASTA OU DIGITARㅤ**

## Clear
Serve para limpar o terminal, utilizando: *clear*

## Ls(list)
Lista o que está dentro do diretório, utilizando *ls*

## Ls (list) Al
Lista arquivos ocultos dentro do diretório, utilizando *ls- al*
<-------------------------------------------------------------------------------------------->


# INICIAR UM REPOSITÓRIO
 Para inicializar o git criando os arquivos necessários para inicializar um repositório utiliza-se : *git init*

# ADICIONAR UM REPOSITÓRIO AMBIENTE LOCAL
Para Adicionar o repositório principal ao ambiente local deve-se:

## 1° -  buscar o link do repositório do GitHub
utilizando: *git remote add origin (link)*

## 2° - Para ver as origens já registradas
utilizando: *git remote -v*

## 3° - Para remover a origem atual para adicionar outra
utilizando: *git remote rm origin*

## CLONAR UM REPOSITÓRIO
No GitHub e copia o link do (SSH ou HTPPS), depois utilizar: *git clone*
Copia todos os arquivos do repositório para a pasta selecionada incluindo a pasta
**ㅤPara trazer apenas os arquivos usa-se:ㅤ**
git@github.com:LeonardoAtaides/MyProjects.git . -> *apenas add com o espaço o ponto*
<-------------------------------------------------------------------------------------------->

# VERIFICAR STATUS DO REPOSITÓRIO
Mostra os status dos arquivos do projeto, utilizando: *git status*


# ADICIONAR ARQUIVOS
Ao adicionar qualquer coisa ao projeto é necessário adicionar para salvamento prévio,
utilizando: *git add .*


# COMITAR ARQUIVOS
Após adiocionar é necessário comitar para subir para o reposiotório as alterações e uma descrição sobre as alterações, utilizando: *git commit -a -m "comentário"*


# SUBIR ALTERAÇÕES AO REPOSITÓRIO
Para enviar as alterações ao repositório, utiliza-se: *git push*


# RECEBER ALTERAÇÕES DO REPOSITÓRIO
Para receber alterações do repositório, utiliza-se *git pull*
 

# REMOVER ARQUIVOS DO REPOSITÓRIO
Remove arquivos, não só deletando do GitHub mais também do projeto alocado da máquina local

## Para remover um arquivo após ter dado um *git add*
utiliza-se: *git rm -f (arquivo)*

## Para remover um arquivo após ter dado um *git commit*
utiliza-se: *git rm (nome_arq)*
<-------------------------------------------------------------------------------------------->


# HISTÓRICO DE ALTERAÇÕES
Possibilita acessar as modificações feitas no projeto, utilizando: *git log*
**recebendo informações sobre os commits já realizados no projeto**
                                                ______Mostrando:_______
commit 6eb1549e5be7553cbb                      |    Código do Commit    |
Author: Leonardo Ataídes <leonardo@gmail.com>  | Nome e Email da pessoa |
Date:  Sun Dec 29 17:39:38 2024                |     Data Mês e Hora    |
    delete file                                |   Mensagem do Commit   |
                                               ||
         **Apertando ENTER vai mostrando todas as alterações**

## Histórico Resumido
Mostra um Histórico de alterações de forma resumida, utilizando: *git shortlog*
<-------------------------------------------------------------------------------------------->


# RENOMEAR ARQUIVOS
Possibilita renomear, utilizando: *git mv*
Ex: git mv (pasta)/(arquivo) (pasta)/(novo nome do arquivo)


# MOVENDO ARQUIVOS
Possibilita mover, utilizando: *git mv*
Ex: git mv (arquivo) (pasta)/(arquivo)


# DESFAZENDO ALTERAÇÕES "MOMENTÂNEAS"
O arquivo modificado retorna ao estado original, utilizando: *git checkout*
Ex: Realiza-se uma modificação e decide apagar, mesmo apagando o git identifica uma alteração,
então usa git checkout (arquivo) para retornar ao estado original.


# DESFAZER TODAS AS ALTERAÇÕES
Exclui todas alterações já feitas, inclusive as comitadas, mas quando não foi enviado ao repositório ainda, utilizando: *git reset*, geralmente é utilizado com flag --hard e a origem
Ex : *git reset --hard origin/main*


# IGNORAR ARQUIVOS NO PROJETO
Usado para ignorar arquivos utilizando: *.gitinore*, cria-se um arquivo com este nome e coloca os arquivos os nomes dos arquivos que deseja ignorar
**ㅤÉ NECESSÁRIO ADICIONAR O NOME DO ARQUIVO NO *gitignore* ANTES DE INCLUIR O ARQUIVO NO PROJETOㅤ**


# SALVAR O CÓDIGO EM UMA "LIXEIRA"
Usado para salvar as modificações que talvez não serão usadas no projeto, como uma espécie de lixeira, exclui o código mais tem como recuperar depois, utiliza-se: *git stash*
após utilizar o comando o branch será resetado para a versão de acordo com o repositório
            **ㅤO COMANDO SO FUNCIONA ANTES DE DAR COMMITㅤ**

## VERIFICAR STASHS
Pode-se verificar as stashs criadas pelo comando *git stash list*

## RECUPERAR STASHS
Para recuperar a stash utiliza-se o comando *git stash apply (indice)*

## VER AS MODIFICAÇÕES DO STASH
Para ver as modificações feitas no stash utiliza-se o comando *git stash show -p(indice)*

## REMOVER UM STASH
Para limpar totalmente as stash de um branch, utiliza-se *git stash clear*, para remover uma especifica utiliza o comando *git stash drop (indice)*
<-------------------------------------------------------------------------------------------->


# TAGS
Usada como um checkpoint de um branch, usada para demarcar estágios do desenvolvimento de algum recurso    **ㅤPRECISA COMITAR É DEPOIS SALVAR A TAGㅤ**

## CRIAR UMA TAG
Pode-se criar tags nos branches, utilizando *git tag -a (nome) -m "(mensagem)"*, a tag serve como uma espécie de checkpoint, demarcando pontos do desenvolvimento do projeto

## VER UMA TAG
Para visualizar as tags já criadas utiliza-se *git tag*

## VERIFICAR UMA TAG
Pode-se verificar uma tag com o comando *git show (nome)*
**ㅤPode ser usado para ver detalhes de um commit em branchesㅤ**

## TROCAR DE TAG
Podemos trocar de tags com o comando git checkout (nome)

## ENVIAR A TAG AO REPOSITÓRIO
Podemos enviar as tags para o repositório de código, utiliza-se 
o comando git push origin(nome), para enviar todas as tags usa-se,git push origin --tags
<-------------------------------------------------------------------------------------------->


# SUBMÓDULO
É a maneira de ter dois ou mais projetos em um só repositório. Para isso e é necessário
ter outro repositório para conciliar com o atual

## CRIANDO UM SUBMÓDULO
utiliza-se o comando - *git submodule add <link_do_repositório> submodulo*

## ATUALIZANDO O SUBMÓDULO
utiliza-se o comando - *git push --recurse-submodules=on-demand*, onde fará atualização
apenas do submódulo
<-------------------------------------------------------------------------------------------->


# LIMPANDO ARQUIVOS UNTRACKED
E usado para verificar os arquivos que não estão sendo trackeados e removendo eles, utilizando *git clean -f*
**ㅤImportante e sempre adicionar os que deseja logo após utilizar o comando  *clean*ㅤ**
**ㅤArquivos trackeados são aqueles de não foram adicioandos ao *git add* aindaㅤ**

# OTIMIZANDO O REPOSITÓRIO
Para otimizar o repositório, utiliza-se o comando *git gc*, que identifica arquivos que não são mais necessários e os exclui, onde ajuda a otimizar o projeto

# CHECAR A INTEGRIDADE DO REPOSITÓRIO
Para verificar a integridade dos arquivos e sua conectividade, utiliza-se o comando *git fsck*, **VERIFICA POSSÍVEIS CORRUPÇÕES EM ARQUIVOS**

# REFLOG
Usado para mapear todos os seus passos no repositório, até uma mudança de branch é inserida neste log, utilizando o comando *git reflog*
**FICAM SALVOS DURANTE 3O DIAS ATÉ EXPIRAREM**

# TRANSFORMAR O REPOSITÓRIO PARA ARQUIVO
Para transformar o repositório em um arquivo, utiliza-se o comando
*git archive --format zip --output master_files.zip (branch)*, criando um arquivo zipado

# COMMIT PRIVADO EM UMA BRANCH
Onde é criado branch que não será compatilhada no repositório, então pode-se fazer qualquer commit, utilizando o *rebase* com o comando:
*git rebase (branch atual) (branch-privado) -i*, escolhendo branches pra excluir *(squash)* e renomear com *(reword)* e depois para salvar no arquivo digita *;xl!*

# GITHUB
 
# ABA ISSUE
Permite criar tarefas ou possíveis bugs do projeto, se tornando algo crucial 
a organização e se manter ciente do que precisa *fazer ou corrigir*