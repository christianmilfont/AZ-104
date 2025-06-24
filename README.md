# AZ-104
### Curso DIO para tirar certificação da AZ-104

### Objetivo geral:
Executar os conhecimentos necessarios para o papel de administrador da Azure complementando as capacidades de gerenciar recursos, armazenamento, computação e redes virtuais em um ambiente nuvem!

### Conteúdo programático:
2. Administrar Governança e Conformidade

## Roteiro de Aprendizagem:
- Configurar Assinaturas
- Configurar o Azure Policy
- Configurar o Controle de Acessos baseado em função (Famoso RBACK)
![image](https://github.com/user-attachments/assets/f34d2afc-95c9-4eea-bf67-64a7e9c99064)


## Identificar Regiões
- As regiões da Azure vão ter empresas e data centers que irão se conectar rapidamente Back Bone da Microsoft
- No Brasil tem apenas uma região soberana que seria em São Paulo, e a replicação que temos no Rio de Janeiro serve para alguns serviços mas necessita consultas a disponibilização para Microsoft
- Uma região ela representa uma coleção de datacenters(geralmente usa a estratégia de 3 datacenters)
- Fornece flexibilidade e escala, podendo determinar que um produto fique apenas um desses datacenters ou disponibilizar replicação nos 3
- Preservar a residencia de dados
- Relacionado a velociade de acesso as informações, sejam priorizados os datacenters sejam mais proximas dos usuarios
- Os preços eles variam entre regiões
- No Brasil tem muitas taxas
- Há serviços globais que são independentes da região

## Implementar Assinaturas
![image](https://github.com/user-attachments/assets/f4bcb250-2555-4b59-bba4-1e1c57abf45c)
- Mesmo eu tendo uma conta, eu posso ter mais de uma assinatura
- Somente identidades no Azure AD ou em um diretório confiável pelo Azure AD podem criar uma assinatura
- A unidade lógica de serviços do Azure que está lincada a uma conta do Azure (como se fosse uma subscrição)
- Criar várias assinaturas vai ajudar a limitar o cenário de segurança e limitar gastos

## Identificar o uso da assinatura
![image](https://github.com/user-attachments/assets/7c3367de-b4f0-466f-8bfb-61b309c3358d)
- Enterprise, esse modelo de contrato é o mais difícil de se conseguir, o ponto é por conta do alto valor, ela vai ter descontos em diversos recursos e tem que apresentar toda a documentação provando que ela está em dia
- CSP, funciona como uma empresa parceira que atenda dentro daquele nicho, buscar o parceiro mais qualificado que atenda minha necessidade, ele vai fazer uma ponte entre a Microsft e o cliente
- Pré pago, mais voltado para testes
- Aluno, a Microsoft Students fornece algumas licensas como o pacote office por exemplo

## Criar Grupos de Recursos
![image](https://github.com/user-attachments/assets/763f2357-3e10-4a7c-a6a6-4d07a5106cca)
- Cada grupo de recursos podem ser organizado em pastas de recursos
- Cada recurso tem uma precificação
- Os recursos so podem existir em um unico gurpo de recurso
- Eles não podem ser renomeados nem aninhados, caso for necessário terá que criar um novo grupo e passar os dados do antigo para esse novo
- Os grupos podem ter recursos de muitos tipos diferentes (serviços) e de muitas regiões diferentes
- Voce pode movimentar recursos entre grupos
- Cotas e limites de serviços
![image](https://github.com/user-attachments/assets/03c7d86d-be19-40fb-81ec-dc6e84a9cd49)
- Caso extrapole a cota de serviço pode-se abrir um CASO DE SUPORTE pedindo para Microsoft para aumentar o limite daquele recurso expecífico

## Hierarquia de recursos no Azure e marcações
![image](https://github.com/user-attachments/assets/8ed4d312-075b-4773-8653-bfa7d5d93157)
- Os grupos de gerenciamento do Azure fornecem um nível de escopo sobre assinaturas
- Direcionamento de políticas e gastos entre assinaturas e heranças nas hierarquias
- Implementar relatórios e custos por organização (empresas/equipes)
### Marcação ou Tags de Recursos:
- Fornece metadados aos Recursos do Azure
- Item não obrigatório
- Ajuda no rateio e para Organizar logicamente os recursos para varias coisas, principalmente para filtrar quando chega as cobranças
- Ajuda no gerenciamento e mapeamento de custos da Empresa, separando as assinaturas e projetos por Tags

## Gerenciar Custos
![image](https://github.com/user-attachments/assets/62066848-bcfb-4c99-b3ea-f5cd421f32d1)
- Os custos são específicos dos recursos 
- Os custos de uso podem varias entre os locais
- Os custos das transferencias de dados de entradas e saída diferem
- Pre pagar com as intancias reservadas do Azure
- Usar licensas do On-premise com o benefício híbrido do Azure
- Otimizar com alertas, orçamentos e recomendações do Assistencia do Azure
  
## Criar um resource group:
- Adicionar a subscrição
- Adicionar a região
- Ele é apenas uma caixa organizadora
- Container Lógico onde eu vou colocar os recursos
![image](https://github.com/user-attachments/assets/6094cf0e-61ae-4a8d-8bd4-fbf2493d9f75)
- Posso criar sem colocar tag pois não são obrigatórias
- Não preciso de recursos da mesma região
### Usage = Quotes:
- Lá teremos uma ideia de quanto recursos podemos ter por localidade
- Adicionar no resgister providers um registro registrado
- Quando exceder o limite, tem que abir uma solicitação de new quote, e adicionar um novo limite
- Faz diretamente pelo portal essa solicitação de novo limite
![image](https://github.com/user-attachments/assets/dc29d312-7f52-4df3-a76c-801e3286a6bc)

## Hierarquia de Ambiente
- 4 níveis de hierarquia
- O grupo de gerenciamento raiz, ele é criado automático
- Permisionamentos são herdados
![image](https://github.com/user-attachments/assets/3ce806ae-6627-40d2-9634-c7ff5c5d9c56)
- Grupo de gerenciamento sempre acima da assinatura
### Tag ela é um modelo não herdavel
- Para que todos recursos do meu resource group tenham a mesma tag, é necessário atribuir uma police (uma política)

# Configurando o Azure Policy 
- O Azure Policy dentro do Azure, são um serviço para criar, atribuir e gerenciar políticas
- Executa avaliações e varreduras e busca de recursos não compatíveis
- Se assemelha aos GPO's dos ambientes On-premises
- São atribuidos pelas empresas times específicos para adicionar essas politicas do Azure (Time de infra ou time de nuvem)
- Vai usar para pradonizar o ambiente
![image](https://github.com/user-attachments/assets/8238a0a5-06b7-4f2b-9b57-133e2df0a20d)
- A politica atribui regras para todos os tipos de permissionamento, seja owner ou mais basicos, não conseguem criar algo que a politica barrou
- Regras aplicadas a todos
## Criando Politicas do Azure
![image](https://github.com/user-attachments/assets/f37e0611-98dd-48fd-a875-52b8b5314732)
- Iniciativa seria um conjunto de politicas, aplicada em momentos exemplo: Criar uma nova assinatura e adicionar as politicas a elas, não precisaria adicionar uma por uma mas sim apenas apontar aquela iniciativa para essa nova assinatura
- Escopo e atribuição, para adicionar é la no managment group ou em um resource group
### As regras de negócios descritas nas Polices são descritas em qual formato?
- JSON
### O que é necessário fazer quando a política não está sendo aplicada corretamente no Azure?
- Verificar se a política está habilitada, pois ela pode não estar ativa.
#### ❌ "Remover os recursos da assinatura..."
- → Isso não resolve nada, e pode causar perda de dados. A política deve ser configurada corretamente para agir sobre os recursos, não o contrário.

#### ❌ "Alterar a assinatura de recursos..."
- → Recursos não são movidos entre assinaturas só para aplicar políticas. As políticas é que devem ser atribuídas no escopo correto.

#### ❌ "A política precisa ser deletada e recriada..."
- → Isso não é necessário na maioria dos casos. Normalmente, ajustar a atribuição ou configuração da política já resolve.

![image](https://github.com/user-attachments/assets/d9c08d89-fa4c-45de-ba45-b3f5444b8955)

## Funções do RBAC vs Azure AD
![image](https://github.com/user-attachments/assets/e07bac5f-7db0-4ad4-a1b5-fca9f385eb89)
- O RBAC (Controle de Acesso Baseado em Função) gerencia as permissões de acesso dos usuários aos recursos no Azure, garantindo que eles possam acessar apenas os recursos necessários para suas funções.
- Diferente do Azure Policy, no RBAC é atrelado as pessoas, ja que ele analisa também ao cargo e permisionameto da pessoa que esta tentando acessar

## Criar uma definição de função
![image](https://github.com/user-attachments/assets/2be48e69-fd79-4680-9a9b-4f407d469b41)

- Garante permisionamentos de diferentes formas como, ir diretamente na assinatura e dentro do resource group adcionar e dizer o nivel de acesso, ou tambem diretamente num recurso especifico
- Os tipos de permisionamento que costumam cair frequentemente em provas é PROPRIETARIO COLABORADOR E LEITOR
- Proprietario ele é o dono, ele quem criou a conta ou seja o Owner, ele pode invitar, lida tambem com o escopo de permisionamento
- Reader ou leitor, não tem permissao nenhuma, apenas le
- Colaborador ou Contribuitor tem acesso de alteração, deletar adicionar, dentro do cenário, mas não tem como atribuir permisionamento a outras pessoas
- Adicionando mais detalhes, vendo o slide acima, demonstra que ele em Actions tem o * que representa tudo, em NotActions, ele possui Authorization delete e Write, alem do elevar acesso, entendemos como estou dando acesso, tirando ou aumentando, que nesse caso ele é proibido
### Criar uma atribuição de função
![image](https://github.com/user-attachments/assets/4b68007f-47b9-427e-8bc6-8b3e1f8468de)
- Definição de função
- Atribuição de função
- Escopo
- sempre mantendo o permisionamento mais granulado possivel

## Aplicar autenticação RBAC
![image](https://github.com/user-attachments/assets/bf215428-1850-4d19-ad4d-fc98d81cfc8e)
- Os permisionamentos que a pessoa deu para o user no Microsoft Entra ID, não se aplica aos recursos
