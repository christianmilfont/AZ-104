# AZ-104
### Curso DIO para tirar certificação da AZ-104

### Conteúdo programático:
5. Administrar conectividade entre sites

![image](https://github.com/user-attachments/assets/e5d27056-423f-4eda-9988-142ccad69031)
- Gateway de VPN permite o transito de gateway
- Serve para meu ambiente On-premises, ja que ela aponta para meu local
- Alem de ter o peering ele tem uma conexao que faz com que a rede da sub net chegue ao meu ambiente on-premise
- O transito de gateway permite que redes virtuais emparelhadas compartilhem o gateway e tenham acesso a recursos
- Nenhum gateway VPN é necessario na rede virtual spoke emparelhada
- o emparelhamento de VNet padrao fornece conectividade total
- Sem esquecer dos padroes de espacos de endereco de IP de redes conectadas, que nao podem se sobrepor
- O tráfego entre máquinas virtuais em redes virtuais com peering é roteado diretamente através da infraestrutura de backbone da Microsoft
- O peering de VNets permite conectar redes virtuais de forma privada, fácil e com baixa latência, porem o transito de gateway nao é automaticamente permitido globalmente, logo o transito nao pode ser configurado globalmente
- Usar rotas do sistema para redirecionar o tráfego da Internet para os servidores locais da sua empresa para inspeção de pacotes
- As redes virtuais não podem existir em qualquer região de nuvem do Azure
- Garantir que você selecione um SKU de gateway apropriado para criar uma conexao entre duas redes virtuais
- Emparelhamento reginal e global são os dois tipos
- Para controlar o fluxo de tráfego na sua rede virtual do Azure voce deve usar uma rota personalizada em uma rede virtual
- Para garatnir comunicacao entre as redes virtuais em regioes diferentes, utilizando a infra do backbone da microsoft, que traz desempenho e seguranca é necessario usar o emparelhamento de Vnets entre diferentes redes virtuais
- Emparelhamento regional é o emparelhamento de Vnet é feito entre redes virtuais na mesma região
- Quando emparelhamento de Vnet, entre uma rede virutal e outra, quer garantir a verificação da resposta da cominucacao seja enviada e que nao tenha dificuldade para testes de conectividade, é necessario configurar a comunicacao reversa tambem
- No laboratório, qual é a principal razão para se usar o conceito de Vnet de hub e spoke?
- Para segmentar redes e isolar serviços, aumentando a segurança e evitando a comunicação entre Vnets sem necessidade.
- Criar um emparelhamento global entre as Vnets é a configuração necessaroa para que as que estejam em regioes diferentes possam comunicar-se entre si utilizando o emparelhamento 
- As rotas definidas pelo usuário permitem que o administrador personalize o tráfego de rede, enquanto as rotas de sistema são criadas automaticamente pelo Azure
- Pontos de extremidade de serviço são usados para limitar o acesso à rede e permitir comunicação entre máquinas virtuais dentro de uma rede virtual, sem precisar de acesso à internet
- A tabela de rotas define um conjunto de regras para o tráfego de rede dentro da sub-rede, podendo substituir ou adicionar rotas de sistema padrão
