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

  As informações são adcionadas a camado do TCP à medida que o pacote o atravessa, e este processamento é conhecido como  encapsulamento e o inverso dele é o desencapsulamento.

  Uma carácteristica do TCP é a de que ele é baseado em conexão, o que significa que ele deverá estabelecer uma conexão entre um cliente e um dispositivo atuando como um servidor antes dos dados serem enviados.
Por causa disto o TCP garante que qualquer dado será enviado e recebido pelo outro lado. Este processo é chamado de Three-Way-Handshake.

  Aqui estão algumas de suas vantagens:
  1. Garante a integridade dos dados;
  2. Capaz de sincronizar dois dispositivos para evitar que um seja inundado de dados na ordem errada;
  3. Realiza os processos com confiabilidade.

  Agora algumas desvantagens:
  1. Requer uma conexão confiavel entre os dois dispositivos. Se um pequeno pedaço de informação não for recebido, então todo o pedaço sera corrompido e deverá ser reenviado;
  2. Uma conexão lenta pode estrangular outro dispositivo, pois a conexão será reservada em outro dispositivo o tempo todo;
  3. É significativamente mais lento que o UDP, pois mais trabalho tem que ser feito pelos aparelhos usando este protocolo.

| **Cabeçalho**             | **Descrição**                                                                                                                                                                    |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Porta Fonte               | Esse valor é a porta aberta pelo remetente para enviar o pacote TCP. Este valor é escolhido aleatoriamente (fora das portas de 0–65535 que ainda não estão em uso no momento).   |
| Porta Destino             | Este valor é o número da porta que um aplicativo ou serviço está executando no host remoto (aquele que recebe dados); por exemplo, um servidor web rodando na porta 80. Ao contrário da porta de origem, esse valor não é escolhido aleatoriamente. |
| Fonte IP                  | Este é o endereço IP do dispositivo que está enviando o pacote.                                                                                                                  |
| Destino IP                | Este é o endereço IP do dispositivo ao qual o pacote é destinado.                                                                                                                |
| Sequência Número          | Quando ocorre uma conexão, o primeiro dado transmitido recebe um número aleatório.                                                                                               |
| Número Reconhecimento     | Depois que um dado tiver recebido um número de sequência, o número do dado seguinte terá o número de sequência + 1.                                                              |
| Checksum                  | Esse valor é que dá integridade ao TCP. É feito um cálculo matemático onde a saída é lembrada. Quando o dispositivo receptor realiza o cálculo, os dados devem estar corretos; caso contrário, serão considerados corrompidos. |
| Dados                     | Este cabeçalho é onde os dados, ou seja, bytes de um arquivo que está sendo transmitido, são armazenados.                                                                        |
| Flag                      | Este cabeçalho determina como o pacote deve ser tratado por qualquer um dos dispositivos durante o processo de aperto de mão. Bandeiras específicas determinarão comportamentos. |

  Agora as principais mensagens especiais usadas durante a comunicação desse processo:

| **Etapa** | **Mensagem** | **Descrição**                                                                                                                                         |
|-----------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1         | SYN          | Uma mensagem SYN é o pacote inicial enviado por um cliente durante o handshake. Este pacote é usado para iniciar uma conexão e sincronizar os dois dispositivos. |
| 2         | SYN/ACK      | Este pacote é enviado pelo dispositivo receptor (servidor) para reconhecer a tentativa de sincronização do cliente.                                   |
| 3         | ACK          | O pacote de reconhecimento pode ser usado tanto pelo cliente quanto pelo servidor para confirmar que uma série de mensagens/pacotes foi recebida com sucesso. |
| 4         | DATA         | Uma vez que a conexão foi estabelecida, os dados (como bytes de um arquivo) são enviados através da mensagem "DATA".                                  |
| 5         | FIN          | Este pacote é usado para encerrar a conexão de forma limpa (adequada) após sua conclusão.                                                            |
| #         | RST          | Este pacote encerra abruptamente toda a comunicação. É usado como último recurso e indica que houve algum problema no processo. Por exemplo, se o serviço ou aplicação não estiver funcionando corretamente ou se o sistema tiver falhas como falta de recursos. |

  Qualquer dado enviado recebe uma sequência numérica aleatória e é reconstruido essa sequência númerica e incrementando em 1. Ambos dispositivos devem concordar com a mesma sequência númerica para que os dados sejam enviados na ordem correta.

| **Dispositivo**    | **Sequência Numérica Inicial (ISN)** | **Sequência Numérica Final**    |
|--------------------|--------------------------------------|---------------------------------|
| Cliente (Emissor)  | 0                                    | 0 + 1 = 1                       |
| Cliente (Emissor)  | 1                                    | 1 + 1 = 2                       |
| Cliente (Emissor)  | 2 (2)                                | 2 + 1 = 3                       |

  Primeiro o TCP fechará uma conexão depois que um dispositivo determinar que o outro recebeu com sucesso todos os dados. Para iniciar o encerramento da conexão, o dispositivo enviará o pacote "FIN" para o outro dispositivo, e o TCP irá reconhecer este pacote.

## UDP/IP
  












