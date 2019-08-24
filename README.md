# Projeto_Azure 
Como subir maquinas pelo Azure usando terraform

Objetivos:

 Provisionar uma máquina virtual no Azure usando Terraform para automação utilizando o Visual Studio Code.

Ferramentas usadas:
- Linux ou Windows,
- Terraform,
- Azure,
- Shell Script, para automatizar a execução,
- Visual Studio Code.

Passo a Passo:

### Passo 1 - Ativadondo o Cloud Shell do Azure


>  Cloud Shell do Azure não vem habilitado você terá que ativa o mesmo para usar, essa ativação tem um gasto pois quando ativado ele cria Storage V2 para funciona

Usar o Azure Cloud Shell
O Azure hospeda o Azure Cloud Shell, um ambiente de shell interativo que pode ser usado por meio do navegador. O Cloud Shell permite usar bash ou PowerShell para trabalhar com serviços do Azure. É possível usar os comandos pré-instalados do Cloud Shell para executar o código neste artigo sem precisar instalar nada no seu ambiente local.

Para iniciar o Azure Cloud Shell:

 - Selecione Experimente no canto superior direito de um bloco de código. Selecionar Experimente não copia automaticamente o código para o Cloud Shell.	Exemplo de “Experimente” no Azure Cloud Shell
 - Acesse https://shell.azure.com ou clique no botão Iniciar o Cloud Shell para abri-lo no navegador.	Inicie o Cloud Shell em uma nova janela
Clique no botão Cloud Shell na barra de menus no canto superior direito do portal do Azure.	Botão Cloud Shell no portal do Azure

 
Para executar o código neste artigo no Azure Cloud Shell:

1. Abra o Azure Cloud Shell.
1. Clique no botão Copiar no bloco de código para copiá-lo.
1. Cole o código na sessão do Cloud Shell com Ctrl+Shift+V no Windows e no Linux ou Cmd+Shift+V no macOS.
1. Pressione Enter para executar o código.


### Passo 2  -  Instalar o Azure CLI no Windows

CLI do Azure fornece acesso à CLI por meio do prompt de comando do Windows (CMD), PowerShell ou Bash.

Agora você pode executar a CLI do Azure com o az comando do Prompt de Comando do Windows, PowerShell ou Bash. O PowerShell oferece alguns recursos de conclusão de guias não disponíveis no Prompt de Comando do Windows. Para entrar , execute o comando az login

1. Execute o login comando.
az login

Se a CLI puder abrir seu navegador padrão, ele fará isso e carregará uma página de entrada.

Caso contrário, você precisa abrir uma página do navegador e seguir as instruções na linha de comando para inserir um código de autorização depois de navegar para https://aka.ms/devicelogin em seu navegador.

2. Entre com suas credenciais de conta no navegador.

Para saber mais sobre diferentes métodos de autenticação, consulte Conectar-se ao Azure CLI .



Feito isso voce ja tem acesso ao seu azure pelo terminal tanto do windows quando linux agora vamos instalar o Visual Studio Code e a extensão da conta do Azure fica seu criterio usar ou nao o Visual Studio Code ,mais eu recomento pois essa ferramenta nao e so para o Azure ela tem extenção para outros programas.

### Passo 3 - Conecte-se ao Microsoft Azure diretamente no Visual Studio Code

O Visual Studio Code é um editor de código fonte desenvolvido pela Microsoft para Windows, Linux e macOS. Ele inclui suporte para depuração, controle de Git incorporado, realce de sintaxe, conclusão de código inteligente, snippets e refatoração de código.

1. Instalar a Extenção da conta do Azure
Para começar, no menu de extensões, pesquise a Azure Account e clique em Instalar,Uma vez que instalar a extensão, deve reiniciar o Visual Studio Code.
1. Para acessar o login e usar o Shell de Nuvem do Azure, abra a Paleta de Comandos (Ctrl + Shift + P) ou (F1) e clico no Azure Sign In (Se você não vir, digite Azure) Depois de clicar no Azure Sign In, o seu navegador abrira no site do azure e autentique-se. Agora que autenticou, podera usar o PowerShell ou o Bash para se conectar ao Cloud Shell.

### Passo 4 - Instalar Extenção do Terraform no Visual Studio Code


