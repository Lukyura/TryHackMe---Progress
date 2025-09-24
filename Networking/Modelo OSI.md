# O que é o Modelo OSI?

  O Modelo OSI (Open System Interconnection) é um modelo essecial usado em redes. Este modelo crítico fornece uma estrutura ditando como todos os dispositivos em rede enviarão, receberão e interpretarão dados.
  
  Um dos principais benefícios dele é que os dispositivos pode ter diferentes funções e designs em uma rede enquanto se comunicam com outros dispositivos. Os dados enviados através de uma rede que segue a uniformidade
do modelo OSI podem ser compreendidos por outros dispositivos.
  Consiste em sete camadas, onde cada camada tem um conjunto diferente de responsabilidades. Em cada camada individual que os dados percorrem, processo específicos ocorrem e pedaços de informação serão adicionados.

  O modelo consiste nas seguintes camadas:
 7. Aplicação (Application)  
 6. Apresentação (Presentation)  
 5. Sessão (Session)  
 4. Transporte (Transport)  
 3. Rede (Network)  
 2. Enlace de Dados (Data Link)  
 1. Física (Physical)

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

























  
  
