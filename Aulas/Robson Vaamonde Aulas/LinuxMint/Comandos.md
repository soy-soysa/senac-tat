sudo apt = Comando comum

sudo apt update = Verificar atualizações

sudo apt upgrade = Atualizar o sistema

sudo apt upgrade --fix-missing = corrigir erros de atualizações

sudo apt autoremove = remover aplicativos desnecessários

sudo apt autoclean = remover cachês de aplicativos

sudo reboot = reiniciar o sistema

power off = desligar o sistema

sudo apt install nome-completo-do-aplicativo = instalar um aplicativo

history = histórico de comandos

ls -l = listar os diretorios e arquivos no diretorio atual

ls -lh = transformar o tamanho dos arquivos em bytes em vez de bits

ls -lha = listar TODOS os diretorios e arquivos no diretorio atual (incluindo ocultos)
(palavra em azul = diretorio) (palavra em branco/cinza = Arquivo) (.palavra com ponto = arquivo/diretorio oculto)

cd = navegar entre os diretorios

pwd = exibe o diretorio atual

cd .. = ir para o diretorio anterior ao atual

mkdir <nome do arquivo>= criar um diretorio

echo <escricao do arquivo> > <tipo do arquivo> = cria um arquivo com algo escrito nele

touch <tipo_do_arquivo> = Cria um arquivo vazio

cat <tipo_do_arquivo> = Abre um arquivo em modo leitura

cat -n <tipo_do_arquivo> = Abre um arquivo em modo leitura e numera as linhas

head -n<00> <tipo_do_arquivo> = lista as <00> primeiras linhas do arquivo

tail -n<00> <tipo_do_arquivo> = lista as <00> ultimas linhas do arquivo

mv <nome do diretorio OU tipo_do_arquivo> <nome do diretorio OU tipo_do_arquivo> = mover um diretorio ou arquivo para outro lugar

nano <tipo_do_arquivo> = editar um arquivo de texto (CTRL + O e ENTER para salvar, CTRL + X para sair)

|(piper) = Separar o comando atual para inserir outro na mesma linha

---------------------------------------------

COMANDOS DO GIT (LINUX)

git clone linkdorepositorio = copia um repositorio do g.hub para o win/linux

git config --list = listar alterações feitas

git config --global user.name "nomedogit" = alterar/adicionar o nome do GIT

git config --global user.email emaildogithub = alterar/adicionar o email do GIT

git status = exibe tudo o que foi alterado no git

git add . = adicionar alterações

git commit -m "Atualizacao" = comitar atualizações localmente (requer adicionar alterações)

git pull = donwload do diretório online para pasta local

git push = upload da pasta local para o diretório online (requer comitação local) 
