# Introdução a mensageria na Azure
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

