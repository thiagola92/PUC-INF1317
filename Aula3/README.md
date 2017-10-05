# Aula 3

As redes tinhasm meios para se comunicar entre si (fibra ótica,...), elas podiam ter um intermediario ou não.  

Para classificar a escala da rede, o alcance delas, usamos as seguintes termonologias  
WANs: Wide Area Networks (mundo inteiro)  
LANs: Local Area Networks (local, rede pequena)  
MANs: Metropolitan Area Networks (por exemplo, rede do rio de janeiro)   
SANs: Storage Area Networks (obsoleta)  
CANs: Campus Area Networks (obsoleta, rede da puc)

## Topologia
É a forma como nós arrumamos a comunicação entre os usuários, a escolha de topologia pode afetar muito os usuários.  
Existe dois grandes/famosos métodos de arrumar os meios.  

### Multi-Ponto  
![Multi-Ponto](1.PNG)  
Os dispositivos compartilham uma mesma barra para se comunicarem.  

### Ponto a Ponto  
![Ponto a Ponto](2.PNG)  
Um dispositivo passa informação pra uma pessoa qualquer e essa pessoa passa para o alvo.  
Uma transmissão ponto a ponto pode ser usada de varias maneiras  

Simplex: Uma ligação que você projetou esse meio de maneira que um lado só tem transmissor e o outro receptor, ou seja, só pode usar em um sentido.  
![Simplex](3.PNG)  

Half-duplex: Tem transmissores e receptores em ambos os lados, mas não pode usar os dois ao mesmo tempo, ou seja, enquanto estiver sendo usado para um sentido, não pode ser usado para o outro.  
![Half-duplex](4.PNG)  

Full-duplex: Consegue fazer ambos sentidos ao mesmo tempo  
![Full-duplex](5.PNG)  

### Topologia totalmente ligada
Considerada a melhor topologia em todos os casos, ligar todos a todos.  
![Totalmente ligada](6.PNG)  
Essa topologia deixa você quase sem nenhum problema:  
* Não precisa endereçar ninguém, pois se está sendo transmitido pelo cabo da pessoa X, então a informação é para a pessoa X.  
* A disponibilidade da rede é a maior possivel, pois toda comunicação seria full-duplex, ou seja, se todos quisessem falar com todos ao mesmo tempo, a rede suportaria.  

Qual o problema então? Custo, para cada computador adicionado na rede, teria que adicionar n-1 cabos.  
O total de cabos seria n.(n-1)/2.  

### Topologia parcialmente ligada
A ideia é ter menos cabos mas manter o grafo conexo, ou seja, qualquer um consegue chegar em qualquer um, mas não precisa ser diretamente. Você também não quer reduzir a ponto de tornar uma árvore, isso acabaria deixando 1 caminho sendo obrigátorio para muitos computadores na rede.    
![Parcialmente ligada](7.PNG)
