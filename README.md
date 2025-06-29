# AZ-104
### Curso DIO para tirar certificação da AZ-104


### Conteúdo programático:
4. Administrar rede virtual

## Configurando DNS
- Para adcionar um registro dns, precisa criar\ adicionar um registro TXT ou MX a zona DNS
- O DNS do Azure permite que eu gerencie e hospede seu dominio registrado e registros associados
- Para mapear um ou mais endereços IP em um unico dominio precisa criar ou adicionar um A ou AAAA
```
Registro A (Address) mapeia um nome de domínio para um endereço IPv4.

Registro AAAA mapeia um nome de domínio para um endereço IPv6.

Esses registros são usados para apontar um domínio para um ou mais endereços IP.
```
- Para executar tarefas de gerenciamento de domínio do Azure, você deve ser Administrador Global
- Os nomes de domínio padrão do Azure = domainname.onmicrosoft.com
- Hospedar registros de domínio, como A, CNAME, MX, entre outros, dentro de uma rede virtual é a função de uma zona de DNS no Azure
- Adicionar um registro TXT ou MX no provedor de domínio e realizar a verificação no Azure é necessário para validar que um domínio personalizado no Azure pertence ao usuário
- Traduzir nomes de domínio em endereços IP para direcionar usuários ou sistemas a recursos específicos na rede é o principal objetivo do DNS no contexto do Azure
- Especificar um servidor DNS customizado dentro da configuração da rede virtual é necessário para adicionar um servidor DNS customizado dentro de uma rede virtual do Azure
- Alguns recursos e aplicações não aceitam esse endereço, o que pode gerar falhas na criação de registros é o motivo para não utilizar o endereço "local" (ex: .local) em zonas de DNS privadas no Azure
- Oferecer resolução de nomes dentro de redes virtuais sem acesso à internet pública é a principal vantagem de usar zonas de DNS privadas no Azure
- O nome do domínio alternativo é adicionado, permitindo que ele seja utilizado para criar usuários, isso ocorre após a verificação de um dominio personalizado no Azure
- É necessário ajustar ao criar uma rede virtual Azure (alem do nome e regiao), deve estabelecer faixas de IP e definir as sub redes que vao utilizar
- Definir os intervalos de IP garante que nao haja sobreposicao de IPs com outras redes e que as sub redes funcionem corretamente
- Criar uma regra de segurança de entrada que permita tráfego nas portas necessárias, como 80 e 443 é necessario para permitir o trafego de entrada
