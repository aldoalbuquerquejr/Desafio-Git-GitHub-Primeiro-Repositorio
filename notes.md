# Anotações do Curso Introdutório Git/GitHub :thumbsup: 

### Comentário: "Esta é a segunda vez que assisto esse curso. Quando o assisti pela primeira vez, a mais ou menos 1 ano atrás, tudo era muito nebuloso para mim. Agora, todo o funcionamento e os comandos da plataforma fazem mais sentido.  Nas anotações abaixo, deixo uma lista com os diversos comandos exibidos no curso, assim como alguns algoritmos essenciais pra realização de processos como por exemplo, criar uma chave SSH no Windows e Linux, criar um token de acesso pessoal no Windows e Linux, clonar repositório usando chave SSH ou token de acesso pessoal, etc."

## Anotações:

Comandos de Terminal

comando + TAB : autocomplete 
silence on sucsses = ‘tudo certo’
î : Navegar pelo histórico de comandos utilizados no terminal.
*Pastas que começam com . são pastas ocultas.

1.	Windows:
dir : Listar pastas. (directory)
cd / : Acessar repositório base. (change directory)
cd ‘pasta’ : Acessar a pasta especificada.
cd .. : Retroceder um nível.
cls : Limpar tela/terminal. (clear screen)
mkdir ‘pasta’ : Criar uma pasta. (make directory)
echo ‘texto’ : Retorna o texto especificado.
echo ‘texto’ > ‘texto’.arquivo : Criar arquivo especificado em um formato de arquivo especificado.
del ‘pasta’ : Deletar todos os arquivos da pasta especificada. 
rmdir ‘pasta’ /S /Q : Remover a pasta especificada com todos os arquivos contidos nela. (remove directory)
git –version : Verificar a versão do git instalado na máquina.

2.	Unix:
ls : Listar pastas. (list)
cd / : Acessar repositório base.
cd ‘pasta’ : Acessar a pasta especificada.
cd .. : Retroceder um nível.
clear : Limpar tela/terminal. (clear); Ctrl + L
mkdir ‘pasta’ : Criar uma pasta.  
echo ‘texto’ > ‘texto’.arquivo : Criar arquivo especificado em um formato de arquivo especificado.
rm -rf ‘pasta’ : Remover a pasta especificada com todos os arquivos contidos nela. (remove recursive-force) 
git –version : Verificar a versão do git instalado na máquina.


3.	Git Bash:
   openssl sha1 ‘arquivo’ : Gerar Sha do arquivo especificado. 
   git init : Criar uma pasta git (.git/) vazia dentro do repositório local.
   ls -a : Exibir itens ocultos contidos na pasta local. 
   git config --global user.email “email do usuário” : registrar email do usuário da máquina. 
   git config --global user.nickname “nome de usuário” : registrar nome de usuário do usuário da máquina.  
   git add * : Adiciona todos os arquivos da pasta local à pasta git. 
   git add . : Adiciona todos os arquivos da pasta local à pasta git.
   git commit -m “mensagem” : comitar pasta git com comentário. 
   git config --list : Listar as configurações atuais no do git instalado na máquina. 
   git config --global --unset user.email : Remover o email registrado.
   git config --global --unset user.nickname : Remover o nome de usuário registrado. 
   git remote add origin ‘link do repositório’ : Reconhecer o link do repositório. 
   git remote -v : Listar os repositórios remotos cadastrados. 
   git status : Checar o status do repositório. 
   git push origin master : Empurrar o repositório da máquina para o GitHub. 
   git pull origin master : Puxar um repositório editado do GitHub. 
   git clone ‘link do repositório’ : Clonar um repositório do GitHub para a sua máquina. 
4.	Criar chave SSH no Git (Windows):
   Clicar no ícone da foto (canto superior direito) -> Settings -> SSH and GPG Keys -> New SSH Key -> abrir Git Bash -> ssh-keygen -t ed25519 -C ‘email do usuário’ -> criar passphrase -> cd ‘c/Users/’usuário da máquina’/.ssh/’ -> ls -> cat id_ed25519.pub -> copiar a chave (sequência de caracteres) -> voltar ào GitHub -> dar um título à chave -> colar a chave na caixa ‘Key’ -> Add SSH Key -> voltar ào Git Bash -> eval $(ssh-agent -s) -> ssh-add id_ed25519 -> digitar passphrase -> .
5.	Criar chave SSH no Git (Linux):
   Clicar no ícone da foto (canto superior direito) -> Settings -> SSH and GPG Keys -> New SSH Key -> abrir Git Bash -> ssh-keygen -t ed25519 -C ‘email do usuário’ -> criar passphrase -> cd /home/’usuário da máquina’/.ssh/ -> ls -> cat id_ed25519.pub -> copiar a chave (sequência de caracteres) -> voltar ào GitHub -> dar um título à chave -> colar a chave na caixa ‘Key’ -> Add SSH Key -> voltar ào Git Bash -> eval $(ssh-agent -s) -> ssh-add id_ed25519 -> digitar passphrase -> . 
6.	Clonar repositório do GitHub com chave SSH (Windows): 
   Copiar link SSH do repositório no GitHub -> abrir Git Bash na pasta onde o clone será salvo -> git clone ‘link SSH’ -> autenticar o host com ‘yes’ -> digitar passphrase -> .
7.	Clonar repositório do GitHub com chave SSH (Linux):
   Copiar link SSH do repositório no GitHub -> abrir Git Bash na pasta onde o clone será salvo -> git clone ‘link SSH’ -> autenticar o host com ‘yes’ -> digitar passphrase -> . 
8.	Criar Token de acesso pessoal no Git (Windows):
   Clicar no ícone da foto (canto superior direito) -> Settings -> Developer settings -> Personal access tokens -> Generate new token -> dar um título ào token -> selecionar o tempo de expiração -> marcar a opção repo -> Generare token -> copiar o token e salvar em um local seguro e de confiança -> . 
9.	Clonar repositório do GitHub com token de acesso pessoal (Windows): 
   Copiar link HTTPS do repositório no GitHub -> abrir Git Bash na pasta onde o clone será salvo -> git clone ‘link HTTPS’ -> colar token de acesso pessoal -> Sign in -> .
10.	Criar repositório no GitHub:
    Entrar no GitHub -> Repositories -> New -> criar um nome para o repositório -> adicionar uma descrição -> Create repository -> .
11.	Empurrar um repositório da máquina para o GitHub: 
    Copiar link do repositório no GitHub -> abrir Git Bash na pasta local -> git init -> git add * -> git commit -m “mensagem” -> git remote add origin ‘link do repositório’ -> git push origin master -> . 
