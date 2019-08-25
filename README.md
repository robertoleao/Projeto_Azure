# Projeto_Azure_Terraform
Como subir maquinas pelo Azure usando terraform


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
> O arquivo esta todo comentado para facil entendimento https://github.com/robertoleao/Projeto_Azure/blob/master/Script%20completo%20do%20Terraform

1. Na barra de menus, selecione Arquivo > Salvar Como.
Na caixa de diálogo Salvar como, navegue até um local de sua escolha e, em seguida, selecione o local para salva.

Na caixa de diálogo Salvar Como, altere o nome padrão do arquivo para **main.tf**













