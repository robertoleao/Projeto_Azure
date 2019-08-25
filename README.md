# Projeto_Azure_Terraform
Como subir maquinas pelo Azure usando terraform



Instalar o Azure CLI no Windows

CLI do Azure fornece acesso à CLI por meio do prompt de comando do Windows (CMD), PowerShell ou Bash.

Agora você pode executar a CLI do Azure com o az comando do Prompt de Comando do Windows, PowerShell ou Bash. O PowerShell oferece alguns recursos de conclusão de guias não disponíveis no Prompt de Comando do Windows. Para entrar , execute o comando az login

1. Execute o login comando.

```sh
az login
```
Se a CLI puder abrir seu navegador padrão, ele fará isso e carregará uma página de entrada.

Caso contrário, você precisa abrir uma página do navegador e seguir as instruções na linha de comando para inserir um código de autorização depois de navegar para https://aka.ms/devicelogin em seu navegador.

2. Entre com suas credenciais de conta no navegador.






Feito isso voce ja tem acesso ao seu azure pelo terminal tanto do windows quando linux agora vamos instalar o Visual Studio Code e a extensão da conta do Azure fica seu criterio usar ou nao o Visual Studio Code ,mais eu recomento pois essa ferramenta nao e so para o Azure ela tem extenção para outros programas.

A extensão do Terraform para Microsoft Azure Visual Studio Code foi projetada para aumentar a produtividade do desenvolvedor ao criar, testar e usar o Terraform com o Azure. A extensão fornece o suporte de comando do Terraform, visualização gráfica de recurso e integração do CloudShell com o Visual Studio Code.

Você aprenderá a:

* Use o Terraform para automatizar e simplificar o provisionamento dos serviços do Azure.
* Instalar e usar a extensão do Terraform do Microsoft Visual Studio Code para serviços do Azure.
* Verificar se o Visual Studio Code para gravar, planejar e executar planos de Terraform.
* Criar uma infraestrutura completa de máquina virtual do Linux no Azure usando o Terraform.

Pré-requisitos
1. Assinatura do Azure: Se você não tiver uma assinatura do Azure, crie uma conta gratuita antes de começar.
1. Terraform: instale e configure o Terraform.
1. Visual Studio Code: instale a versão do Visual Studio Code apropriado para seu ambiente.

Preparar o ambiente de desenvolvimento

### Instalar o Git
Para concluir os exercícios neste artigo, você precisará instalar o Git.
### Instalar o HashiCorp Terraform
Siga as instruções na página da Web Instalar o Terraform da HashiCorp, que abrange:
### Baixando o Terraform
Instalando o Terraform
Verificar se o Terraform é instalado corretamente
### Instalar o Node. js
Para usar o Terraform no Cloud Shell, você precisará instalar o Node.js.
### Instalar GraphViz
Para usar a função visualizar do Terraform, será necessário instalar o GraphViz.
### Instalar a extensão do Visual Studio Code do Azure Terraform
1. Inicie o Visual Studio Code.
1. Selecione Extensões.

![alt text](https://user-images.githubusercontent.com/53921314/63644567-5693e980-c6c2-11e9-8f59-251ea9f27505.png)
1. Use a caixa de texto Pesquisar extensões no Marketplace para procurar a extensão do Terraform do Azure:

![alt text](https://user-images.githubusercontent.com/53921314/63644552-ee450800-c6c1-11e9-8054-91f2f3a0739c.png)

Selecione Instalar.
> Quando você seleciona Instalar para a extensão do Terraform do Azure, o Visual Studio Code automaticamente instala a extensão de Conta do Azure. Conta do Azure é um arquivo de dependência para a extensão Terraform do Azure, usado para executar autenticações de assinatura do Azure e extensões de código relacionadas ao Azure.

Depois de instalado agora é possível executar todos os comandos com suporte do Terraform em seu ambiente do Cloud Shell de dentro do Visual Studio Code.


### Preparar o arquivo

1. No Visual Studio Code, selecione Arquivo > Novo Arquivo na barra de menus ou CTRL+N
![alt text](https://user-images.githubusercontent.com/53921314/63644537-91e1e880-c6c1-11e9-8085-def9fc32b0e5.png)

1. Copie o código no bloco de código criado no Visual Studio Code.

> O modelo esta todo comentado para facil entendimento 

https://github.com/robertoleao/Projeto_Azure/blob/master/Script%20completo%20do%20Terraform

1. Na barra de menus, selecione Arquivo > Salvar Como.
Na caixa de diálogo Salvar como, navegue até um local de sua escolha e, em seguida, selecione o local para salva.

Na caixa de diálogo Salvar Como, altere o nome padrão do arquivo para **main.tf**

### Criar e,Implantar a infraestrutura

Com o modelo do Terraform criado, a primeira etapa é inicializar o Terraform. Esta etapa garante que o Terraform tem todos os pré-requisitos para criar o modelo no Azure.

Executar o comando init do Terraform

1. Inicie o Visual Studio Code.
1. Na barra de menus do Visual Studio Code, selecione Arquivo > Abrir Pasta… e localize e selecione o arquivo main.tf.
1. abra a Paleta de Comandos (Ctrl + Shift + P) ou (F1) e digite o comando... > Azure Terraform: init.

![alt text](https://user-images.githubusercontent.com/53921314/63645023-15a0d280-c6cc-11e9-9db5-86dab2e6efd2.png)

Quando a confirmação for exibida, selecione OK.

![alt text](https://user-images.githubusercontent.com/53921314/63645117-d07da000-c6cd-11e9-8d63-7325f2da3667.png)

Na primeira vez que iniciar o Cloud Shell em uma nova pasta, você será solicitado a configurar o aplicativo Web. Selecione Abrir.
A página Bem-vindo ao Azure Cloud Shell será aberta. Selecione Bash ou PowerShell.

![alt text](https://user-images.githubusercontent.com/53921314/63645130-00c53e80-c6ce-11e9-988e-920ee9907bd0.png)

Se você ainda não configurou uma conta de armazenamento do Azure, a tela a seguir será exibida. Selecione Criar armazenamento.

![alt text](https://user-images.githubusercontent.com/53921314/63645148-25b9b180-c6ce-11e9-9a8c-c8f2f8fa8968.png)

O Azure Cloud Shell é iniciado no shell que você selecionou anteriormente e exibe informações para a unidade de nuvem que acabou de ser criada.

![alt text](https://user-images.githubusercontent.com/53921314/63645179-a678ad80-c6ce-11e9-881d-315036893a51.png)

A próxima etapa é fazer o Terraform revisar e validar o modelo. Esta etapa compara os recursos solicitados para as informações de estado salvo por Terraform e, em seguida, gera a execução planejada. Os recursos não são criados no Azure.

terraform plan

Depois de executar o comando anterior, você deverá ver algo semelhante à seguinte tela:

```bash
Refreshing Terraform state in-memory prior to plan...
The refreshed state will be used to calculate this plan, but will not be
persisted to local or remote state storage.

...

Note: You didn’t specify an “-out” parameter to save this plan, so when
“apply” is called, Terraform can’t guarantee this is what will execute.
  + azurerm_resource_group.myterraform
      <snip>
  + azurerm_virtual_network.myterraformnetwork
      <snip>
  + azurerm_network_interface.myterraformnic
      <snip>
  + azurerm_network_security_group.myterraformnsg
      <snip>
  + azurerm_public_ip.myterraformpublicip
      <snip>
  + azurerm_subnet.myterraformsubnet
      <snip>
  + azurerm_virtual_machine.myterraformvm
      <snip>
Plan: 7 to add, 0 to change, 0 to destroy.
```

## Visualizar o plano

Anteriormente neste tutorial, você instalou o GraphViz. O Terraform pode usar o GraphViz para gerar uma representação visual de uma configuração ou plano de execução. A extensão do Terraform do Visual Studio Code do Azure implementa esse recurso por meio do comando visualize.

* Na abra a Paleta de Comandos (Ctrl + Shift + P) ou (F1) e digite o comando... > Azure Terraform: visualize.

![alt text] sem imagem erro


Se tudo estiver correto, e você estiver pronto para criar a infraestrutura no Azure, aplique o modelo no Terraform:

terraform apply

Após a conclusão do Terraform, sua infraestrutura de VM estará pronta. Obtenha o endereço IP público da sua VM com az vm show:
















