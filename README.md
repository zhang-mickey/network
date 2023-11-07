
# Memoryless property
the distribution of a "waiting time" until a certain event does not depend on how much time has elapsed already.  
![image](https://github.com/zhang-mickey/network/assets/145342600/23946553-c72d-458b-a0fb-ae085094800c)

Prob{X>30|given X>10}=Prob{X>20}  
<img width="659" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/cfbaa119-6506-4b23-9476-9169a6e6c60f">

## Exponential Distribution
<img width="599" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/34c695f3-0181-45c1-a481-9d9b24c130e8">

## Erlang Distribution
<img width="595" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/a14938f3-b49c-4fe9-9b2a-810580014029">

## poisson Distribution
<img width="602" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/75c1ab16-3492-4123-9bd8-35fd8f4327bf">

## process (function of time )

## stochastic process
random variables, which are functions of time.  
### types of  stochastic process 
#### Discrete or Continuous state process
#### Markov process
Future states are independent of the past and depend only on  the present.  
Markov chain : discrete state Markov process.  
M/M/m queues can be modeled using Markov processes.  
The time spent by a job in such a quene is a Markov processes, and the number of jobs in the quene is a Markov chain.  
##### Continuous Time Markov Chains (CTMCs)
Poisson arrivals are by far the most popular arrival model used in the analysis of queueing systems.
Markov process > poisson process  


#### Birth-death Process
<img width="600" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/91218ebe-08c8-415b-bb5d-8f413c5a66a3">

#### Poisson process
its fundamental properties is that `arrivals` follow a `Poisson distribution`, and the `time between arrivals` follows an `exponential distribution`.  
<img width="579" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/1926246e-2e62-44d2-b879-a499d8bb3502">

#### Poisson Arrivals See Time Averages(PASTA)
<img width="598" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/0f4752e4-b095-46b3-b63c-bb7435290a4e">


# Quene 
<img width="636" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/66769a70-5475-440a-bc26-82d843d3d6f9">

## arrival process 
<img width="644" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/a96360d6-29b1-452d-aaae-7d6be1059857">  

## service time distribution
<img width="613" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/328d71a0-a26d-4620-ab52-9d94d19238fd">

## service disciplines
<img width="643" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/5d73d7a9-6c72-4acc-9f12-1d8ec5217be5">

## 

## M/M/1
Arrival rate :λ  
The processing rate: μ  
The mean processing time： 1/μ  



## M/M/c queue(multiserver quene)
Arrivals occur at rate λ according to a Poisson process and move the process from state i to i+1.  
Service times have an exponential distribution with parameter μ. If there are fewer than c jobs, some of the servers will be idle. If there are more than c jobs, the jobs queue in a buffer.  
<img width="477" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/961d0a29-1536-4834-95a7-ecee5eac64ac">




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


# Streaming versus elastic traffic
Almost all traffic in todays networks can be classified as being either stream or elastic traffic.
## streaming traffic
has strict bandwidth and delay requirements  
## elastic traffic 

# Literature
High Performance Browser Networking, Ilya Grigorik, O-Reilly, 2013.  
quene theory : https://www.cse.wustl.edu/~jain/queue/index.html  
