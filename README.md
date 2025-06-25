# AZ-104
### Curso DIO para tirar certificação da AZ-104

### Objetivo geral:
- Configurar Recursos do Azure com ferramentas 
- Configurar Recursos com modelos ARM
  
### Conteúdo programático:

3. Administrar recursos Azure

## Comparar Ferramentas de Administrador
- Portal extremamente dinamico
- Ver e gerenciar os recursos
- Interface visual
- Hub unificado - treinamento e documentação
- Personalizar a propria experiencia
- Aplicativo movél
- Acessar o Cloud Shell
- Cenarios de criação unico

## Portal Azure
- Portal torna-se muito mais visual
- Interface bem mais intuitiva
- Documentação dentro da propria pagina do portal explicando

## PowerShell ou Cloud Shell
- Shell interativo acessível pelo navegador
- Oferece Bash ou PowerShell
- É temporário e fornecido por sessão e por user
- Editor de texto gráfico integrado
- Expira após 20 minutos
- Autentica automaticamente
- É atribuida UMA maquina por conta de user
- Requer um grupo de recursos, uma conta de armazenamento e um compartilhamento de arquivos do Azure
- Programas de linha de comando, ou seja, ja tem algumas coisas prontas e ele tem um recurso de auto complete
- Otimiza tempo
- InfrasCode
- Cmdlets e modulos, seguem convenção de nomenclatura verbo-substantivo; enviado em modulos
- Modulos são um arquivo DLL com o codigo para processar cada cmdlet
- Disponivel como isntalacao local no Linux, MacOs e Windows
- Possui um modo interatitvo e de scripts
- O produto base do PowerShell e o módulo Az precisam estar instalador para permitir a execução local

```
Ao criar um grupo de recursos no Azure usando PowerShell (New-AzResourceGroup) ou a CLI (az group create), você obrigatoriamente precisa fornecer:

Nome do grupo de recursos (-Name ou --name)

Localização onde os recursos serão criados (-Location ou --location)

```
- Exemplo com PowerShell:
```
New-AzResourceGroup -Name "meu-grupo-teste" -Location "eastus"
```
- Exemplo com Azure CLI:
```
az group create --name meu-grupo-teste --location eastus
```

- Antes de listar ou criar qualquer recurso no Azure via PowerShell, você precisa estar autenticado na sua conta do Azure. - O comando Connect-AzAccount abre uma janela de login para que você insira suas credenciais da conta Azure e estabeleça a sessão.
```
Os outros comandos:
Get-AzSubscription: só funciona depois de estar autenticado.

Get-AzResourceGroup: só retorna grupos depois do login.

New-AzResourceGroup: só pode criar após autenticação.
```

- Pergunta importante:
```
Suponha que você esteja criando um aplicativo de edição de vídeo que oferecerá armazenamento online para conteúdo de vídeo gerado pelo usuário. Você armazenará os vídeos em Blobs do Azure, portanto, precisará criar uma conta de armazenamento do Azure para conter os blobs. Depois que a conta de armazenamento estiver instalada, é improvável que você a remova e recrie, pois isso excluiria todos os vídeos do usuário. Qual ferramenta provavelmente oferecerá a maneira mais rápida e fácil de criar a conta de armazenamento?
- Portal do Azure
```
![image](https://github.com/user-attachments/assets/60b0efc5-6e98-4dd5-b022-e2a11ec1b16e)
- Sempre pergunta ou bash ou powershell
- Necessita de um Storage Account para usar o recurso dentro dessa sessão

### Caso for usar o Azure CLI, precisa instalar as versões e pacotes para sua maquina e sistema operacional 


## Vantagens modelo ARM
![image](https://github.com/user-attachments/assets/937eda5e-b1fa-4d99-aba1-29ed21c3e8f0)
- Aumenta a produtividade dentro do Time
- Por conta da automatização
- Ajuda no processo profissional de infraestrutura como codigo
- Redução de tarefas manuais diminuindo chance de erro
## Parâmetro modelos Json
![image](https://github.com/user-attachments/assets/0e591bd4-ef49-403e-8e68-8e08d2bfbabc)
- Trabalhando em cima de um Schema
- com uma cadeia de caracteres
![image](https://github.com/user-attachments/assets/2ec0a848-4b08-45fc-88f0-fa2e2269fc86)
- Parametros com detalhamentos, meta-dados e esconde dados sensiveis
- Especifica quais valores são configuraveis quando o modelo é executado
- Dois parametros, um para o nome da VM e outro para a Senha

## Arquivos do BICEPS
![image](https://github.com/user-attachments/assets/da0fde32-4c17-47e6-82ec-f09a394e3378)
- Arm template não é a melhor opção para quem esta começando
- Bicep foi criado para simplificar a sintaxe para escrever modelos
- Arquivos de modulo menor que voce pode referenciar a partir de um modelo principal
- Detecta automatico dependencies dentro dos recursos
- Bicep funciona apenas para Microsoft Azure
- Extensão do VS code com validation e IntelliSense
- Não é como um Terraform que é muilt cloud, mas sim apenas dentro do Azure
- Um documento JSON com pares de valores-chave, é a melhor opção para o Azure Manager
- Um arquivo JavaScript Object Notation (JSON) que define a infraestrutura e a configuração para sua implantação é um modelo do Azure Resource Manager
- Caso eu precise implantar mais uma vez um modelo mas sem alterações, O Azure Resource Manager não fará alterações nos recursos implantados.
![image](https://github.com/user-attachments/assets/d53ceed4-240f-4fbd-926a-1b6185581a4e)
![image](https://github.com/user-attachments/assets/e01cb517-da64-4a5f-bcd0-9212c3eda7cd)
- Traz o codigo de template que estamos usando, no caso do ARM Template
- Schema, trzendo a referencia que é um JSON
- Traz os parametros
- Localização
- Modelo de Aplicação
- Todos os recursos e items relacionados
![image](https://github.com/user-attachments/assets/167e7728-3daa-458d-b0f3-ecb0bc75bfec)
- Exemplo do uso do Bicep
### Automatizar a criação de recursos com menor dependência do portal, tornando o processo mais ágil e repetível é o objetivo principal ao utilizar modelos do Azure Resource Manager (ARM)
