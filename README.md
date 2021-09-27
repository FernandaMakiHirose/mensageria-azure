# Introdução a mensageria na Azure
## Requisitos
- C#
- .NET
- Visual Studio ou Terminal

## Executar o projeto
1. Faça o clone do projeto
2. Compilar e executar a aplicação em `mensageria-azure\scr\livedio`:
>dotnet run

## Mensagens
- Mensagem é composta por um pacote de dados brutos
- Os dados podem estar em diferentes formatos: XML, Json, Bytes

## Eventos
- O evento é uma notificação leve de uma condição ou de uma alteração de estado

## Conclusão
- O editor da mensagem possui uma expectativa sobre como o consumidor manipula a mesma
- O editor do evento não tem expectativa sobre como o evento é manipulado. O consumidor do evento decide o que fazer com a notificação

## Filas
- As mensagens são enviadas e recebidas a partir de filas
- As filas armazenam mensagens até que o aplicativo de recebimento esteja disponível para recebê-las e processá-las

## Por que utilizar filas?
- Transferência de dados
- Separação de aplicativos
- Amortecimento de carga
- Balenceamento de carga

## Tópicos
- Os tópicos de um modo geral são semelhantes as filas, sua principal diferença é poder ter várias assinaturas independentes

## Event Grid
- O Event Grid é uma ferarmenta da azure direcionada para suportar uma arquietura orientada a eventos
- Utilizando um modelo Pub/Sub

## Criar um service bus
- Abra o portal da Azure > Barramento de serviço > (Adicione um serviço) > (Preencha os dados em Criar Namespace) > (Linkando o projeto com o Visual Studio) > (Crie Filas) > (Crie Tópicos e Assinaturas) > (Crie a Assinatura do Evento)
- No Visual Studio adicione o plugin `Microsoft.Azure.ServiceBus` para consumir mensagens do service bus

<details>
  <summary><strong>Quiz</strong></summary>
## O que são mensagens e que em formatos podem estar?
Uma mensagem é composta por um pacote com dados brutos e pode estar em diversos formatos, como XML, JSON, Bytes, entre outros

## O que seria o NuGet?
Mecanismo com suporte da Microsoft para compartilhamento de código, pelo qual é possível obter pacotes úteis, como o Service Bus

## O que é o Azure Service Bus?
Um mediador de mensagens totalmente gerenciado, confiável e seguro para a transferência assíncrona de dados, podemos utilizar filas e tópicos para envio e recebimento de mensagens

## Como as mensagens são enviadas de um serviço para outro?
A mensagem é enviada pelo remetente, armazenada pelas filas, até que outro consumidor pegue essa mensagem como receptor e seja processada

## O que é o Event Grid?
Ferramenta da Azure direcionada para suportar uma arquitetura orientada de eventos. Baseada em um modelo Pub/Sub

## Qual a principal diferença entre mensagens e eventos?
Uma mensagem espera ser manipulada pelo consumidor, já o evento não possui nenhuma expectativa sobre como o evento é manipulado, portando o consumidor do evento decide o que fazer com a notificação

## O que são as filas?
Podemos dizer que são pacotes de armazenamento, onde as mensagens são mantidas até que o aplicativo de recebimento esteja disponível para recebê-las e processá-las

## É possível criar filas do Barramento de Serviço?
Sim, utilizando o próprio portal do Azure é possível criar um namespace, fila de barramento de serviço e obter credenciais de autorização de um aplicativo cliente pode usar para enviar/receber mensagens de/para a fila

## O que são tópicos?
Semelhantes as filas, porém existe uma diferença em poder ter várias assinaturas independentes

## Por que utilizar as filas?
Transferência de dados, separação de aplicativos, amortecimento de carga, balanceamento de carga, entre outros
