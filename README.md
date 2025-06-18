# AZ-104
### Curso DIO para tirar certificação da AZ-104
### Objetivo geral:
Executar os conhecimentos necessarios para o papel de administrador da Azure complementando as capacidades de gerenciar recursos, armazenamento, computação e redes virtuais em um ambiente nuvem!

### Conteúdo programático:
1. Administrar Identidade

Como configurar o Microsoft Entra Id?
1. Descrever os Benefécios e Recursos do Microsoft Entra Id
2. Descrever os conceitos do Microsoft Entra ID
3. Comparar o Microsoft Entra ID com os Active Directory Domains Services (Comparação da autenticação na nuvem e dos ambientes on-primeses)

Como funciona os Planos e Preços do Microsoft Entra ID?
1. Selecionar Planos e preços do Microsoft Entra ID
2. Configurar Identidade de Dispositivo
3. Implementar a Redefinição de Senha por Autoatendimento

## Benefícios e recursos do Entra ID
- Um conjunto de recursos de gerenciamento de identidades baseado em nuvem que permite gerenciar com segurança o acesso aos serviços do Azure para seus usuários
- Entra ID é = Família de Produtos relacionados a Autenticação da Microsoft
- Diferente das Árvores de ambientes on-primeses (os directorys, até mesmo o Azure tinha o Azure Directory) a Microsoft expandiu para uma switch de aplicações relacionadas aos nossos users
- Exemplo disso é que se a pessoa tem o cargo de Admin de Usuarios, ela não precisa entrar em outros recursos mas sim pelo Entra ID

![image](https://github.com/user-attachments/assets/bea7f8f8-2a43-4a5a-a825-e5c22472e952)
Exemplo de modelo de autenticação que passa pelo que chamamos de "protocolo", nesse caso o Kerberos e o NTLM
- No momento que solicita acesso, ele faz uma consulta pertinente ao seu ambiente, confere usuario e senha depois passa para autenticação
- Nesse caso, seria a implementação do Windows Server e Active Directory que fazer esses conferes (modelo legado pois ja esta a muito tempo)
- Mas saindo dos ambientes on-primeses e indo para nuvem, o novo representante é justamente o Entra ID
- Trabalhando outros modelos de autenticação
- Para que os dois modelos de autenticação se conversem, eles precisam do intermediário, o qual seria uma aplicação que faz a autenticação de usuários e grupos + Autoricação

## Conceitos do Entra ID:
```
- Identidade  = um objeto que pode ser autenticado (algo ou alguem que pode ser)
- Assinaturas do Azure= Usada para pagar pelos serviços e recursos de nuvem do Azure
- Conta = Uma identidade que tenha dados associados a ela
- Conta do Microsoft Entra ID = Identidade criada na Nuvem, sendo um serviço na nuvem do Microsoft ou alguma conta criada para finalidade específica
- Locatário/Diretório = Vamos ter uma instancia dedicada e confiavel, podendo criar os meus recursos, mas sendo sempre uma unica instancia onde eu vou representar minha organização.
Exemplo: criar uma conta no Microsoft ADD, automaticamente eu terei um dominio associado a essa conta.
Podemos ter diretorios diferentes para separar os seviços,
e nesse diretorios eu posso associar as Assinaturas do Azure
```

### Entra ID vs ADDs (Active Directory)
- O Microsoft Entra ID é uma solução de identidade, centralizando o gerenciamento dos usuários, grupos e dispositivos do ambiente
- Trabalha em cima de autenticação HTTP
- Consutalndo usando a API REST sobre HTTP e HTTPS
- Já que a maioria das aplicações usam o modelo de API's REST para fazer a conexão
- Como visto anteriormente temos os protocolos HTTP E HTTPs atualizados como o SAML, a especificação Web Services Federation e o OpenID Connect para autenticação ( e o OAlth para autorização)
- Inclui serviços de federação e muitos serviços de terceiros (como o proprio Facebook)
- Autorizando a entrada pelo Facebook, um exemplo (BTC Buissness to Costumer)
- Os usuários e grupos do Microsoft Entra ID são criados em uma estrutura plana(todos na mesma unidade "no mesmo barco"), deferente dos ADDS, não possuem Unidades Organizacionais (OUs) ou Obejtos de Política de Grupo (GPOs)

## Planos e Preços do Entra ID
4 modelos gratuitos: 
- Gratuita
- P1
- P2
- Governança
![image](https://github.com/user-attachments/assets/caedb192-7be3-400d-b01c-4c2942eebdba)

## Configurar identidades de dispositivo
![image](https://github.com/user-attachments/assets/be3c2227-bccd-418d-900e-45a60b6c5264)
- Suporta o Modelo BYOD ou Bring Your Own Device
- Login de dispositivos registrados usando uma conta da Microsoft
- Anexado a uma conta que concede acesso a recursos
- Controle usando ferramentas de gerenciamento de dispositivos moveis (MDM), como o Microsoft Intune
- SO - Windows 10+, iOS, Android e MacOS

### Dispositivos Associados:
![image](https://github.com/user-attachments/assets/550c6a60-ccbf-4341-9960-9fb90be98804)
- Destinado a organizações que priorizam a nuvem ou apenas a nuvem
- Dispositivos de prioridade da organização
- Conta organizacional necessária
- Pode usar políticas de acesso condicional
- SO - dispositivos Windows 10+

### Mais comum atualmente = Dispositivos Hibridos
![image](https://github.com/user-attachments/assets/4a944a90-3fcf-441e-bd1f-fa0cf05d4565)
- Comunicam no On-Primeses e na Nuvem
- Possui aplicativos Win32 implantados nestes dispositivos
- Continua usando Política de Grupo para gerenciar dispositivos
- SO - dispositivos Windows 7+

## Implementando o SSPR
- Self Service
- A redefinição de senha não necessariamente ficar dependente de um atendimento ao pessoal TI mas sim um autoatendimento
- Escolher um numero de métodos de autenticação necessários e os métodos disponiveis
- Exigir cadastro dos usuários no SSPR (mesmo processo do MFA)
![image](https://github.com/user-attachments/assets/db4884f8-7a8f-4a5f-8cd3-f8f8efca2047)
- Tela no qual esse processo de configuração (Admin de Redes)
- Nessa tela mostra os métodos de autenticação (1 ou 2)
- Modelos de autenticação SSPR:
![image](https://github.com/user-attachments/assets/c1f61a04-a504-4ee8-9717-f16b99071cd9)
- Perguntas podem ser de 3 a 5 a serem cadastradas
- E quantas dessas perguntas podem aparecer depois


## Funcionalidades do Entra ID e criação de Contas de Usuário
- Informações básicas
![image](https://github.com/user-attachments/assets/79aa5173-ed9b-4ab2-ba67-ea20e24060c0)

- O primary domain sempre sera um email opcional, nunca deixa de existir

### Funcionalidades do Entra ID:
- Users: da parte de user possui um Audit Logs, All users e reset de senha, ou seja, Logs e Resets de Senha(Self Service Password Reset SSPR)
- Quando excluir um user existe um tempo de 30 dias para restaurar, fica tambem na func de Users
- Também possui a parte de Grupos, esses grupos são diferente do ambiente on-primeses, podendo criar um grupo de Segurança(Atribuição de uma função) ou do Microsoft 365(interação com o pessoal da empresa, exemplo, grupo tecnologia, grupo relacionado para aqueles da área de tech)
- Também temos as Roles e Acessos: pode dar o permisionamento, mas não o de acessar recursos
- Access Review: Garante que as pessoa do meu time tenham o permisionamento que elas devem ter

### Criado uma conta de user nova:
![image](https://github.com/user-attachments/assets/86ed4fc6-5a59-4ef2-b625-86924474c16d)
- Manter o autogenerate: ver qual a melhor opção para sua empresa, sendo anotar a senha ou voce criar a propria dele
- Account Enabled: melhor deixar apenas na véspera da entrada dessa pessoa na empresa, pois mesmo com email e senha, se essa opção não estiver marcada, ela não consegue entrar
#### Propriedades:
![image](https://github.com/user-attachments/assets/ae3e6c63-953f-4c73-80e5-a6c277c58b56)
![image](https://github.com/user-attachments/assets/95dd6f1a-3576-4226-bbe8-74453a6e4f0a)
- Sempre melhor colocar o Usage Location, pois futuramente exigir uma autenticação para que os signins seja apenas no País do user, ou até mesmo um monitoramento desses signins

#### Assignments:
![image](https://github.com/user-attachments/assets/cebddf2b-6201-4f1d-9a73-2203c54aa723)


#### Ao criar um user externo, ele invita com um email:
![image](https://github.com/user-attachments/assets/239fb6b6-fd4b-4cf5-a07c-a277720c755e)

## Ativação da licensa Premium da Conta P2:
- Necessita de uma conta nativa do meu Tenant (Locatorio)
![image](https://github.com/user-attachments/assets/ba3cba5c-98aa-46bc-866d-e675f509c647)
![image](https://github.com/user-attachments/assets/277758ab-24ec-4023-b05d-eb91677f4534)
- Importante lembrar que o que querremos é o Manager Trial
![image](https://github.com/user-attachments/assets/dd8e57e1-cf14-45c1-b129-06c1993bc869)
![image](https://github.com/user-attachments/assets/aa2b5eae-3a1d-47c5-912b-efd97124acac)
![image](https://github.com/user-attachments/assets/3c2c754d-c6a4-45b4-b78e-e6ad17f6269a)
- Ele pede agora para adicionar informações
- E adicionar Cobrança
![image](https://github.com/user-attachments/assets/b3f39ebe-3a67-459f-b6b9-eccb41da9d49)
- Da pra utilizar o CNPJ da Microsoft
- Adicionar antes um método de pagamento
![image](https://github.com/user-attachments/assets/7dd2b4ae-98af-49a0-945f-332958603739)

### Resumo:
- Adionar a conta interna User como Global Admin
- Fazer Login com essa conta
- Solicitar o Trial da P2
- Configuração dos Dados
- CNPJ pode utilizar o da própria Microsoft
- Depois, voltar ao portal da 365 e remover o método de pagamento
- Depois no portal Azure, remove a permissão de Global Administrator
 
