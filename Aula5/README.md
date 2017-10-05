# Aula 5

## LANs
Qual é a idéia de uma rede local? Fácil de usar e pouca infra estrutura. Não precisar de toda a lógica que as redes tem (virtua/tim...), não precisa de roteamento.  

Quais os 3 métodos princípais de LANs?  
* Barra  
* Anel  
* Estrela  

### Barra 
![Barra](1.PNG)  
A idéia é que qualquer um pode transmitir e essa transmissão vai correr por toda a barra, ou seja, passar por todos conectados. Não precisa de um intermediário cuidando da informação.  
Que problema você já ve de cara? Tudo que você transmite, chega em todo mundo (físicamente).  
Para solucionar o problema de todos ficarem lendo informações que não os interessa, criamos a noção de pacote onde botamos o endereço de destino no cabeçalho e criamos um hardware em cada computador que verifica se o pacote é para ele, se for passa para o usuário princiapl, se não joga fora a informação.  
Mas se quisermos mandar para todos? Teremos que mandar varias vezes e cada pacote com o endereço de destino certo? Para resolver isso criamos um endereçamento especial que equivale a **broadcast**, dessa forma os hardware além de lerem o que tem o endereço deles, vai ler o que for broadcast.  

**Unicast**: Para alguém específico  
**Broadcast**: Para todos lerem  
**Multicast**: Para mais de uma pessoa porém não todas  

Se uma pessoa desativar a parte do hardware que filtra pelo endereço, a pessoa entra em um modo **espião** pois vai poder ler qualquer mensagem que receber.  

Duas estações podem começar a transmitir ao mesmo tempo, quando isso ocorre as informações acabam por se **colidir**, quando se colidem a informção vira lixo. Para solucionar isso, precisamos usar algum tipo de controle, no caso vamos fazer todos usarem uma mesma política para evitar colisão (ou seja, antes de transmitir vai obdecer uma regra).  
**MAC**: Medium Acess Control  

### Anel 
![Anel](2.PNG)
No anel cada estação tem uma interface, um lado dessa interface só transmite, no outro só recebe. Isso cria um fluxo/sentido de transmissão, igual a um simplex, e todos no anel precisam seguir o mesmo fluxo.   
A interface verifica se o pacote é pra ela, se for ela lê.  

Algumas pessoas acham que no momento que ela lê, ela não repassa mais a informação, isso está incorreto. A interface sempre passa o pacote a diante.  
