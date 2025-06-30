# AZ-104
### Curso DIO para tirar certificação da AZ-104


### Objetivo geral:
Executar os conhecimentos necessarios para o papel de administrador da Azure complementando as capacidades de gerenciar recursos, armazenamento, computação e redes virtuais em um ambiente nuvem!

### Conteúdo programático:
11. Administrar monitoramento


### Slide do desafio feito de maneira interativa:
- Cenário do Laboratório 
![image](https://github.com/user-attachments/assets/af4d2818-eb3c-43ec-a182-998e5a993818)
- Com 4 Tasks de Alerta e Trigger


## Implementando Monitoramento no Azure
#### Funções do admin do Microsoft Azure:
- Envio de alertas
- Criação de Triggers
- Grupos de ações (tomar atitude quando servidor estiver fora de contexto)
- Administrar e visibilidade de ações externas

### De primeiro momento:
![image](https://github.com/user-attachments/assets/01e58723-197a-4ab6-adb9-ec4016b39446)
- Ir em Deploy a Costum Template
- Fazendo deploy padrão
![image](https://github.com/user-attachments/assets/f3fbfc87-1159-4fbb-905d-e4c9eb2d1a44)
- Load File para fazer o load do arquivo .JSON
![image](https://github.com/user-attachments/assets/20e1b86b-6695-4a25-bc42-dd4de0c8b845)
- Após fazer o Load do template JSON, adicionar os detalhes e configs restantes
- Dessa forma criando a Infraestrutura inicial, para prosseguirmos validando os proximos topicos
![image](https://github.com/user-attachments/assets/4c83e9f1-c4c5-4fca-bcca-c9607184ca90)

### Configurando Azure Monitor para as VMs
![image](https://github.com/user-attachments/assets/ae898a37-a342-4614-b375-5b026096ec74)
![image](https://github.com/user-attachments/assets/e39c2d62-1003-4c37-9dd4-a3ec06b73809)
-  Clicando em 'View', habilitar o Enable Insights na maquina
![image](https://github.com/user-attachments/assets/3593d5e0-5384-44a8-a6f0-4601beb2f8f8)
![image](https://github.com/user-attachments/assets/9cdf32cb-68c5-4e69-8b5b-239ccbdcc40e)
![image](https://github.com/user-attachments/assets/ce249390-c57c-4ed8-876a-ac6d29ae3b31)

- Manda um agente para nossa maquina e faz com que ela seja monitorada

### Criando os Alertas
![image](https://github.com/user-attachments/assets/b24b79a4-e834-4bff-84d5-f137a8e0e30a)
![image](https://github.com/user-attachments/assets/ac0d4c18-772d-407e-a43f-8c3e66904ab1)
- Seleciona nosso escopo que no caso seria onde vamos aplicar essa regra (Resource Group)
- Em Condition teremos que buscar por todos os sinais, que no caso seria para a condicao "Delete Virtual Machine"
![image](https://github.com/user-attachments/assets/c52a25fd-7c81-4e1d-a40e-8b894a90ba41)
- Em meu alert logic, deixamos All Select em todos
![image](https://github.com/user-attachments/assets/57feb885-cb3c-4879-918f-a50658f1a8e3)

- Em Actions, criaremos um Action Group para provisionar qual ação sera validada
![image](https://github.com/user-attachments/assets/5e0021bf-eb9a-4047-9f49-d6b472875eac)
- Selecionando Resource Group correspondente
- Região = Global
- Selecionando o tipo de notificação
![image](https://github.com/user-attachments/assets/9561f061-93e1-4226-bf92-7c9d50ea2d5a)

#### Nossa estratégia então ficoi: Cada alerta que acontecer vai ser enviado por email quando a máquina for excluida
![image](https://github.com/user-attachments/assets/da04678a-c27b-466a-8675-5adb5feaca48)
