# Pacotes e Quadros

## O que são Pacotes e Quadros?

  São pequenos dados que ao se juntarem foram uma informação ou mensagem maior. No entanto, são duas coisas diferente dentro do modelo OSI.

  Um pacote é um dado da camada 3 (Network) contendo informações como o Header do IP e a carga util, um quadro no entanto é usado na camada do (Data Link), que irá encapsular o pacote e adicionar informações extras
como o endereço MAC.

  Podemos pensar neste processo como algo semelhante ao envio de uma carta pelos correios, onde o envelope seria o quadro, que vai ser usado para mover o conteudo (neste caso o pacote) do envelope para outro lugar,
uma vez que o recptor abre o envelope, ele saber encaminhar a propria carta. Esse processo é chamado de encapsulamento, neste estágio é seguro assumir que quando estamos falando de endereços IP, estamos falando de
pacotes, quando a informação de encapsulamento é retirada, estamos falando do quadro.

  Pacotes são uma maneira eficiente de se comunicar dados através de dispositivos em rede, como esses dados são trocados em pequenos pedaços, há menos chance de ocorrer gargalos em uma rede.
  Por exemplo, ao carregar uma imagem de um site, ela não é enviada para o seu computar com um todo, mas sim pequenos pedaços onde ela é reconstruída no seu computador. Os pacotestem estruturas diferentes que dependem,
do tipo do pacote que será enviado, a rede está cheia de padrões e protocolos que atuam como um conjunto de regras para como o pacote é tratado em um dispositivo. Com bilhões de dispositivos conectados, as coisas
podem se quebrar rapidamente se não houver uma padronização.

  Alguns header de pacote notáveis são

  1. Time to Live (TTL) -> Este campo define um temporizador de validade do pacote, para não sobrecarregar sua rede caso ele nunca chegue ao destino ou escape;
  2. Checksum -> Fornece uma verificação de integridade para protocolos, com TCP/IP, onde se algum dado for alterado, esse falor será diferente do esperado, logo corrompido;
  3. Source Address -> O endereço IP do dispositivo que o pacote está sendo enviado, para que os dados saibam para onde voltar;
  4. Destination Address -> IP do dispositivo para o qual o pacote está sendo enviado, para que os dados saibam para onde viajar em seguida.

## TCP/IP e o Three-Way-Handshake

  Esse protocolo é semelhante ao modelo OSI, e consiste em quatro camadas e é indiscutivelmente apenas uma versão resumida do OSI, esssa camadas são:

  1. Aplicação (Application)
  2. Transporte (Transport)
  3. Internet (Internet)
  4. Interface de Rede (Network Interface)

  As informações são adcionadas a camado do TCP à medida que o pacote o atravessa, e este processamento é conhecido como  encapsulamento e o inverso dele é o desencapsulamento
