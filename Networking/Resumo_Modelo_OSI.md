# O que é o Modelo OSI?

  O Modelo OSI (Open System Interconnection) é um modelo essecial usado em redes. Este modelo crítico fornece uma estrutura ditando como todos os dispositivos em rede enviarão, receberão e interpretarão dados.
  
  Um dos principais benefícios dele é que os dispositivos pode ter diferentes funções e designs em uma rede enquanto se comunicam com outros dispositivos. Os dados enviados através de uma rede que segue a uniformidade
do modelo OSI podem ser compreendidos por outros dispositivos.
  Consiste em sete camadas, onde cada camada tem um conjunto diferente de responsabilidades. Em cada camada individual que os dados percorrem, processo específicos ocorrem e pedaços de informação serão adicionados.

  O modelo consiste nas seguintes camadas:
  
  Aplicação (Application)  
  Apresentação (Presentation)  
  Sessão (Session)  
  Transporte (Transport)  
  Rede (Network)  
  Enlace de Dados (Data Link)  
  Física (Physical)

  Agora veremos um pouco mais das camadas:

## Camada Física (Physical):
      
  Esta é a camada mais facil de se ter uma noção sobre, ela faz referência aos componentes fisicos do hardware usado na rede, e é também a camada mais baixa do modelo, os dispositivos desta camada usam
sinais elétricos para transferir dados entre sim em um sistema de númeração binária.

## Camada de Enlaçe de Dados (Data Link)

  A cada de enla~e de datos, concentra-se no endereçamento da físico da transmissão, ele recebe um pacote da camada de rede (incluindo o IP) e adiciona no físico (MAC) o endreço do endpoint receptor. Dentro de cada
dentro de cada computador hablidade para a rede está a NIC (Network Interface Card) que vem com o endreço MAC exclusivo para identifica-lo, como vimos esses endereços MAC são definidos pelo fabricante e são
literalmente queimados físicamente no cartão, o que torna impossivel a alteração deles, embora possam ser fasificados (spoofing). Quando a informação é enviada através de uma rede, na verdade é o endereço físico que
é usado para identificar onde exatamente enviar a informação. 

  Além disso, também é função da camada de enlace, apresentar os dados em um formato adequado para a transmissão.

## Camada de Rede (Network):

  É a terceira camada do modelo, e é onde a magia acontece e a remontagem dos dados ocorre, em primeiro lugar o roteamento simplesmente determina o caminho ideal no qual esses dados que serão
remontados serão enviados.
  Embora alguns protocolos nesta camada determinem exatamente qual é o melhor caminho, só devemos pensar sobre sua existência nesse estágio do módulo. Resumidamente falando, esses protocolo incluem,
o OSPF (Open Shortest Path First) e o RIP (Routing Information Protocol). Os fatores que decidirão qual rota deverá ser tomada são dedidos da seguinte forma:

1. Qual é o caminho mais curto? Aquele que tem a menor quantidade de dispositivos que o pacote precisa viajar através.
2. Qual o caminho mais confiável? Aquele que não possui menos perda de pacotes.
3. Qual caminho tem a conexão física mais rápida? Caminhos que possuem conexões de cobre são mais lentos, enquanto caminhos que usam fibra são consideravelmente mais rapdidos.

  Nesta camada tudo é tratado por meio de endereços IP. Dispositivos como roteadores são capazes de entregar pacoste usando endereços IP e são conhecidos como dispositivos de terceira camada, pois são capazes de
trabalhar na terceira camada do modelo.]

       [Computador A] ---> [Roteador 1] ---> [Roteador 2] ---> [Computador B]

## Camada de Transporte (Transport):

  A quarta camada do modelo OSI desempenha um papel vital na tranmissão de dados através de uma rede e pode ser relativamente dificil de entender, é baseada em dois protocolos diferentes que são decididos com base em varios fatores.

  O primeiro deles é o TCP (Transmission Control Protocol) este protocolo é projetado com confiabilidade e garantia em mente, e reserva uma conexão constante entre os dois dispositivos entre os dois dispositivos pela mesma quantidade
de tempo que os dados levam para serem enviados e recebidos.
  Não só isso como ele também incorpora verificação de erros em seu design, essa verificação é como o TCP pode garantir que os dados enviados a partir dos pequenos pedaços na camada 5 foram então recebidos e remontados na mesma ordem
  Possui as seguintes vantagens:

  1. Garante precisão de dados;
  2. Capaz de Sincronizar Dois dispositivos para evitar que um deles seja inundado com dados;
  3. Realiza mais processos para garantir confiabilidade

  Mesmo com suas vantagens ele ainda possui pontos negativos, vejamos:

  1. Requer uma conexão confiavel entre dois dispositivos, caso um pequeno pedaço de dados não for recebido, então o dado como um todo será corrompido;
  2. Uma conexão lenta pode atrapalhar outro dispositivo, pois a conexão será reservada no computador recptor o tempo todo;
  3. TCP é significativamente mais lento que o UDP porque mais trabalho tem que ser feito pelos aparelhos que usam este protocolo.

  O TCP serve para situações como o compartilhamento de arquivos, navegação na internet ou envio de e-mails.

  Agora vamos falar um pouco sobre o UDP (User Datagram Protocol), este protocolo não chega a ser tão avançado quanto ao seu irmão, da mesma forma que não possui tantos recursos quanto, tais como verificações de erro e confiabilidade,
na realidade qualquer dado enviado via UDP é enviado para o computador, quer ele chegue la ou não. Portanto não há sincronização entre os dois dispositivos ou garantia, embora isso possa parecer desvantajoso, eles tem seus meritos:

  1. Possui uma conexão mais rápida que a do TCP;
  2. Deixa a camada de aplicação decidir se há algum controle sobre a rapidez com que os pacotes são enviados;
  3. Não reserva uma conexão continua em um dispositivo com o TCP faz.

  Da mesma forma que o TCP, ele também tem suas desvantagens:

  1. UDP não importa se os dados serão recebidos;
  2. É bastante flexivel para desenvolvedores de software neste sentido;
  3. Conexões instaveis resultam em uma experiência terrivel para o usuários.

  O UDP é util em situações onde pequenos dados estão sendo enviados, por exemplo em protocolos utilizados para a descoberta de dispositivos (ARP e DHCP) ou arquivos maiores, como streaming de vídeo (onde está tudo bem se alguma parte do video é pixelada)

## Camada de Sessão (Session)

  Na camada 5 uma vez que os dados tenham sido corretamente traduzidos ou formatados a partir da camada de apresentação (6), esta camada começará a criar e manter a conexão com outro computador para o qual os dados são destinados,
quando uma conexão é estabelecida, há a criação de uma sessão. Embora essa conexão esteja ativa a sessão também estará.

  É também responsável por fechar a conexão se ela não for usada há algum tempo ou se for perdida, além disso, uma sessão pode ter "Checkpoints", onde caso os dados sejam perdidos será apenas necesssário enviar os dados mais novos, o que economiza banda.
  O que é digno de nota é que sessões são unicas, significa que os dados não podem viajar em sessões diferentes, mas na verdade, apenas em cada sessão em vez disso.

## Camada de Apresentação (Presentation)

  É a camada a qual a padronização começa a ocorrer, como os desenvolvedores podem desenvolver qualquer software bem como um client de e-mails, os dados ainda precisarão ser tratados da mesma maneira, não importa o software funcione.

  Esta camada atua como um tradutor para dados e também para a camada de aplicação (7), o computador receptor também entenderá os dados enviados para um computador em um formato destinado a outro formato. Por exemplo, quando você envia um e-mail, o outro 
usuário poderá ter um client de e-mails diferente, mas ainda sim o conteúdo exibido será o mesmo. Recursos com criptografia de dados (como o HTTPS) ocorrem nesta camada.

## Camada de Aplicação (Application)

  Esta é a camada que você está mais familiarizado, e isto ocorre porque é nela que os protocolos e regras estarão em vigos para determinar como o úsuario deverá interagir com os dados enviados ou recebidos.

  Aplicações diárias, como clients de e-mail, navegadores ou software de navegação de servidor de arquivos, como o FileZilla, oferecem um serviço de interface amigavel o GUI (Graphical User Interface) para que os usuários interajam com os dados 
enviados ou recebidos. Outros protocolos incluem DNS (Domain Name System) que é basicamente como os endereços de sites são traduzidos para endereços IP, se o DNS não existissem não digitariamos "github.com" e sim um endereço IP.






















  
  
