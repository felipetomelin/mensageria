# Mensageria - Estudo sobre mensagerias

## Definição 
- O processo de mensageria tem como objetivo realizar a comunicação entre sistemas. Ele é agnóstico ao tipo de mensagem e normalmente possui diversos mecanismos de distribuição e contingência.

### Conceito basico
- Realizar a transação de dados entre serviços.
- Ex: Ao invés de fazer a comunicação entre dois serviços diretamente via rest tendo a possibilidade de qualquer um dos serviços estar fora e quebrar com o fluxo, são criados eventos e publicados em uma fila paralela aos serviços, que serão publicados/consumidos assim que os serviços estiverem no ar de novo.

![Mensageria conceito](https://user-images.githubusercontent.com/50843648/190840053-e330168c-273d-4d6a-a1af-83f49457895d.png)

#### PUB / SUB
- Basicamente é quem faz a publicação e o consumo da mensagem, com o publisher sendo quem publica e o subscriber quem consome, estando inscrito no canal.

![PUBSUB](https://user-images.githubusercontent.com/50843648/190840650-fb888312-50d3-4f0a-ad60-08a41c6654ca.PNG)

#### Dead Letter Queue (DLQ)
- Quando a mensagem tem um erro na sua entrega a mensagem para não ser descartada é movida para a fila DLQ, saindo assim de sua fila principal e futuramente possa ser reprocessada por quaisquer motivos.

![DLQ](https://user-images.githubusercontent.com/50843648/190840654-f4480428-7a7b-4c50-9748-f4276f4cd904.PNG)

#### Request-Reply Pattern
- A solicitação de rotina/processamento é feita ao servidor por um canal e seu retorno depois de processada é feita por outro canal de comunicação.

![Request-Reply Pattern](https://user-images.githubusercontent.com/50843648/190840658-1751f8d2-2d4d-4bc7-9aaf-189edd0defcd.PNG)

## Ferramentas mais famosas
- RabbitMQ
- Apache Kafka
- ActiveMQ
- Azure Service Bus
- NetMQ
- Redis
- Amazon SQS
