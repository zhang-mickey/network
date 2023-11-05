# Memoryless property
the distribution of a "waiting time" until a certain event does not depend on how much time has elapsed already.  
![image](https://github.com/zhang-mickey/network/assets/145342600/23946553-c72d-458b-a0fb-ae085094800c)

Prob{X>30|given X>10}=Prob{X>20}  
<img width="659" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/cfbaa119-6506-4b23-9476-9169a6e6c60f">

## Exponential Distribution

## Poisson Arrivals See Time Averages(PASTA)


# Continuous Time Markov Chains (CTMCs)

Poisson arrivals are by far the most popular
arrival model used in the analysis of queueing systems.

# 
`Latency`:The time from the source sending a packet to the destination receiving it  

`bandwidth`: Maximum throughput of a logical or physical communication path  
`Throughput`: actually achieved bandwidth  
<img width="486" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/8ab65b69-5f07-4e26-9a20-2fe41048b996">

# TCP
`in-order delivery`  
`packet error checking`  
<img width="569" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/bb3d38c0-424b-41c0-9c21-707f4431f182">
</br>

## TCP fast open
allows data transfer within the SYN packet,

### flow control
prevent the sender from overwhelming the receiver with data it may not be able to process  
`receive window(rwnd)`  
each ACK packet carries the latest rwnd value for each side.  
<img width="639" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/3e89baff-5d77-4def-b6c0-6092cc403b32">

### slow start
flow control prevented the sender from overwhelming the receiver, but there was no mechanism to prevent either side from overwhelming the underlying network:   
neither the sender nor the receiver knows the available bandwidth at the beginning of a new connection.  
`congestion window size(cwnd)`  
The maximum amount of data in flight for a new TCP connection is the minimum of the rwnd and cwnd values  
### congestion control 

### congestion avoidance
TCP is specifically designed to use packet loss as a feedback mechanism to help regulate its performance.  
until a packet is lost, at which point the congestion avoidance algorithm takes over.    

<img width="555" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/7629c800-2158-4aa9-8ac0-8e1b339af0d1">

### Bandwidth-Delay Product(BDP)
the current receive windowsare communicated in every ACK, and the congestion window is dynamically adjusted by the sender based on the congestion control and avoidance  
 algorithms.


 
# UDP
Applications that can deal with out-of-order delivery or packet loss and that are latency
or jitter sensitive are likely better served with an alternate transport, such as UDP.

# TLS
<img width="466" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/375ff171-ed3e-4b5d-9b5b-dea16e89c774">
</br>
three essential services:  
`encryption`
`authentication`
`data integrity`  

## TLS handshake 

# Literature
High Performance Browser Networking, Ilya Grigorik, O-Reilly, 2013.
