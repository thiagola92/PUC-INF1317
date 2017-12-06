# OSI
Segue o princípio de "dividir para conquistar", criar diversas camadas onde cada uma se responsabiliza por uma tarefa.  
Cada camada utiliza os serviços da camada abaixo e oferece serviços a camada acima.  
Cada camada supõe que qualquer erro de fora dessa camada, vai ter sido tratado fora dessa camada e o que recebe não tem erro.  
O padrão de como cada camada recebe ou passa informação permite a alteração da camada em si sem alterar as outras.  
Com isso torna muito mais fácil modificações na rede sem alterar tudo ou quebrar algo.  

# Camadas
O modelo OSI propoem dividir em 7 camadas.

* **Aplicação**
* **Apresentação**
* **Sessão**
* **Transporte**
* **Rede**
* **Enlace**
* **Físico**

# Transferência de dados
![Transferência de dados](1.gif)  

Como pode ver cada camada acrescenta mais informação ao pacote da pessoa que quer transmitir dados, por sua vez o receptor tem essas mesmas camadas justamente para ler essas partes de informações.  
Algumas camadas podem botar apenas no ínicio do seu pacote a informação extra, outras botam no ínicio e no fim... Cada camada segue seu estilo, o que importa é que o receptor saiba como é.  
![Transferência de dados](1.png)  

SDU (**Service Data Unit**) são os dados recebidos justamente da camada de cima, sem ter tido qualquer alteração.  
PDU (**Protocol Data Unit**) são os dados já encapsulados no protocolo da camada. Esse é passado para a próxima camada como o SDU dela.  
![SDU PDU](2.png)  

# Físico
* Transmissão de bits através de um canal de comunicação (cabo/wifi/...)
* Características do meio físico e da transmissão do sinal
  * Características mecânicas
  * Características elétricas
  * Características funcionais
  * Características procedurais
  
# Enlace
* Detecta e opcionalmente corrige erros que por ventura ocorram no nível físico (dessa maneira aumentando a confiabilidade da informação)
  * Quando detectar erro (e não conseguir corrigir) deve-se jogar a informação fora, a camada acima não deve receber informação incorreta/corrompida...
* Transmissão e recepção de quadros (delimitação)
* Controle de fluxo

# Rede
* Roteamento (decidir o caminho do pacote até o destino)
* Encaminhamento

# Transporte
* Fornece uma comunicação fim-a-fim, ou seja, elas não passam nenhuma informação que é útil para as camadas abaixo, a informação dela é útil apenas para a própria camada
  * Detectação de erros fim-a-fim
  * Controle de fluxo fim-a-fim (opcional)
  * Recuperação de erros fim-a-fim (opcional)
* Segmentação e remontagem de mensagens

![fim-a-fim](3.jpg)

Por que Transporte precisa fazer detectação de erro? Para verificar se os protocolos justamente dessa camada foram seguidos.  
Por que Enlace precisa fazer detectação de erro se Transporte já faz? Imagina que em alguma parte do caminho deu erro, você apenas jogaria esse dado no lixo quando chegasse na fonte. Mais fácil fazer detectar o mais cedo possível para tirar da rede.  

# Sessão
* Controle de Diálogo
  * Pontos de sincronização
  * Recuperação da sessão em caso de falhas
* Controle dee Atividade
  * Agrupamento lógico de diálogos
  * Cada atividade corresponde a uma tarefa que pode ser interrompida e posteriormente retomada

# Apresentação

# Aplicação

# Tabela
Uma tabela para ajudar você +/- a entender o que fica em cada etapa (usarei apenas coisas mais populares)

| Físico | Enlace | Rede | Transporte | Sessão | Apresentação | Aplicação |
| ------ | ------ | ---- | ---------- | ------ | ------------ | --------- |
| Modem, Wi-Fi, Bluetooth, USB, Cabo... | Ethernet | IP(IPv4, IPv6) | TCP, UDP | ? | ? | HTTP, DNS, BitTorrent |

Wikipedia contém tabelas melhores:  
https://pt.wikipedia.org/wiki/Modelo_OSI  
https://en.wikipedia.org/wiki/OSI_model  
