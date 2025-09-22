# LAN Introdução.

  Uma LAN (Local Area Network) é uma rede usada para conectar dispositivos em um espaço limitado, como casas, escolas ou empresas. Para entender como ela funciona, é importante conhecer alguns pontos principais: as topologias, que mostram como os dispositivos estão organizados; as sub-redes, que ajudam a dividir e organizar melhor a rede; o ARP, que faz a ligação entre endereços IP e MAC; e o DHCP, que distribui automaticamente os endereços IP para cada dispositivo.

## Topologias:

  Ao longo dos anos houve diversos tipos de experimentação no quesito topologia de rede, quando nos referimos a este termo, estamos na verdade falando do projeto ou da aparência da rede em questão
e falaremos das vantagens e desvantagens de certas topologias.

## Topologia de Estrela:

          [Switch]
         /   |   \
     [PC1] [PC2] [PC3]

  Sua premissa principal são os dispositivos estarem conectados através de um outro dispositivo central, como um hub ou um switch, sendo a topologia mais encontrada atualmente devido sua escalabilidade e
confiabilidade, apesar de ter um custo mais alto de manutenção. Nesta topologia, todas as informações enviadas a um dispositivo saem originalmente do dispositivo central onde ele está conectado.

  Por ser uma topologia que exige mais cabeamento e também a compra de dispositivos dedicados de rede, ela possui um custo mais caro que as outras. Porém mesmo possuindo um valor mais alto, ela possui vantagens
significativas em comparação aos outros tipos, como o fato de ser mais escalavel, o que torna mais facil a inclusão de novos dispositivos na rede a medida que a demanda aumenta.
  Infelizmente, quanto maior a escalabilidade da rede, mais dificil fica de se fazer a manutenção da mesma, e isto pode gerar complicações na solução de problemas. Além do fato de que como todas as outras topologias,
ela é sujeita a falhas, embora de forma reduzida, ou seja, se o dispositivo que conecta os outros falhar, nenhum dos dispositivos conseguirá enviar ou receber dados.

## Topologia de Barramento:

           [PC1]       [PC2]       [PC3]
              │           │           │
    ──────────┴───────────┴───────────┴──────────
              │           │           │
            [PC4]       [PC5]       [PC6]


  Este tipo de conexão depende apenas de um unico cabo, conhecido como backbone, se assemelha muito a uma folha de arvore, no sentido de que os dispositivos seriam as folhas e partem do galho que seria o cabo.

  Como todos os dados navegam por um mesmo cabo, ele fica sujeito a uma sobrecarga resultando em lentidão e gargalo caso os dispositivos dentro da rede aceitem dados simultaneamente, e em caso de gargalo
o resultado é uma solução de problemas complicada pois fica dificil de se encontrar o dispositivo que esta com problemas ja que os dados trafegam pela mesma rota.
  No entanto, dito isto esse tipo de topologia são fáceis e economicas de se configurar com custos reduzidos, como cabo e equipamentos de rede dedicados usados para conexão entre os dispositivos.
  
  Por fim, uma ultima desvantagem dessa topologia é a pouca redundância em caso de falhas, isto se deve ao fato de que há um unico ponto de falha ao longo do backbone. Em caso de rompimento do cabo os dispositivos
não conseguiriam mais receber ou transmitir dados.

## Topologia em anel:

      [PC1] ---- [PC2]
       |          |
       |          |
      [PC4] ---- [PC3]
  
  Neste tipo de topologia, os dispositivos também são conectados uns aos outros formando um loop, o que resulta em pouco gasto com equipamento dedicado e cabeamento como em uma topologia estrela.
Ela funciona enviando dados pelo loop até que cheguem ao destino, usando dispositivos ao longo do caminho para encaminhar esses dados, e curiosamente um dispositivo só enviará os dados recebidos
caso o mesmo não tenha dados a serem enviados, caso tenha, ele enviará os proprios dados primeiro.

  Como os dados sempre trafegarão em uma unica direção, é relativamente facil de solucionar falhas eventuais que venham a surgir, no entanto, pode ser uma faca de dois gumes, levando em conta que
essa não é a maneira mais eficiente de se fazer o trafego de dados, pois um dado pode ter que passar por varios dispositivos antes de chegar no destino. Por fim, essas topologias são menos propensas
a gargalos que a de barramento, pois não há trafego de grandes volumes de dados simultaneamente, porém, basta um cabo cortado ou um dispositivo defeituoso e resultará na interrupção de toda a rede.


## Switches:

  São dispositivos dedicados dentro de uma rede, e projetados para agregar varios dispositivos simultaneamente. Esses diversos dispositivos são conectados a porta de um switch. Switchs são geralmente encontrados
em redes maiores, onde existem varios dispositivos para conectar, podendo suportar de 4 a 64 conexões simultaneas.
  São mais eficientes que seus equivalentes menores (hubs/repetidores), por sua capacidade de monitorar as conexões e em qual porta o dispositivo está, facilitando o envio de arquivos diretamente para o destino.

  Switches e roteadores podem ser conectados entre si, assim melhorando a redundacia da rede, com varios caminhos pelos quais o dado pode percorrer, então em caso de falha outro caminho será utilizado. Embora isso
acabe reduzindo de certa forma o desempenho da rede aumentando o caminho percorrido do dado, não haverá tempo de inatividade.

## Roteadores:

  Sua função é exatamente aquilo que seu nome diz, transmitir dados entre dispositivos através do roteamento. 
  Roteamento é o nome dado ao processo de transmissão de dados através de redes, e envolve a criação de um caminho para que esses dados possam ser entregues, sendo utili quando varios dispositivos estão conectados
  em varios caminhos.  

  # Sub-Redes e suas características 


  









  
  
