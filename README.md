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


