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
  
