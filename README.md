`The mean waiting times in an M/G/1 queueing model strongly depends on the variability of the service times,but that the mean sojourn time in the M/G/1 Processing Sharing model in insensitive to the variability.Give an intuitive explanation for this phenomenon`
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
`Why does c CTMS for a queueing model typically assume that inter-arrival times and service times are exponentially distributed?`
```
Exponential distributions have the memoryless property, which means that the probability of an event occurring in the future is independent of past events.  
```
Poisson arrivals are by far the most popular arrival model used in the analysis of queueing systems.
Markov process > poisson process  
#### Kaufman-Roberts recursion
The Kaufman-Roberts functions compute the blocking probability when the total capacity of a link is composed of a
different number of traffic flows or channels, and each flow or channel is smaller than the maximum capacity of the link.  
Kaufman-Roberts is a multi-dimensional Erlang method that you use when multiple services share a common resource pool.  
The Kaufman-Roberts functions compute the blocking probability when the total capacity of a link is composed of a different number of traffic flows or channels. Each flow or channel is smaller than the maximum capacity of the link.  
#### Birth-death Process
<img width="600" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/91218ebe-08c8-415b-bb5d-8f413c5a66a3">

#### Poisson process
`What is a Poisson process and why is it a natural way to model random events?`
its fundamental properties is that `arrivals` follow a `Poisson distribution`, and the `time between arrivals` follows an `exponential distribution`.  
<img width="579" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/1926246e-2e62-44d2-b879-a499d8bb3502">

#### Poisson Arrivals See Time Averages(PASTA)
<img width="598" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/0f4752e4-b095-46b3-b63c-bb7435290a4e">

### little law
the long-term average number L of customers in a stationary system is equal to the long-term average effective arrival rate λ multiplied by the average time W that a customer spends in the system  
The relationship is not influenced by the arrival process distribution, the service distribution, the service order, or practically anything else. In most queuing systems, service time is the bottleneck that creates the queue  
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

## MSS(Maximum Segment Size)
TCP 数据段中数据部分的最大长度
# RTT
从发送方发送数据到发送方接收到来自接收方的确认消息所经过的时间

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

a single link whose capacity is shared by various types of elastic data flows.  
<img width="300" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/0844d10f-700b-4f7f-b34a-447880f09756">



# Voice over IP(VoIP)
a method and group of technologies for voice calls for the delivery of voice communication sessions over Internet Protocol (IP) networks, such as the Internet.  
Instead of being transmitted over a circuit-switched network, the digital information is packetized and transmission occurs as IP packets over a packet-switched network.  
## Packet-switched network
Packets are normally forwarded by intermediate network nodes asynchronously using `first-in-first-out buffering`, but may be forwarded according to some scheduling discipline for fair queuing, `traffic shaping`, or for differentiated or guaranteed quality of service, such as weighted fair queuing or leaky bucket.
Packet switching contrasts with another principal networking paradigm, `circuit switching`, a method which pre-allocates dedicated network bandwidth specifically for each communication session, each having a constant bit rate and latency between nodes.

### traffic policing 
`what are the goals of traffic shaping and policing,and what is the fundamental difference between the two methods?`
<img width="351" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/c1fbbbeb-2ee0-436a-b1fb-b8553e8c7df0">

### traffic shaping

### Jitter buffer
delays packets, put packets in right order   
if too small then packet loss, if too large then packet delay.  

### talker echo
In a telephone conversation a talker sometimes can hear his own voice as a delayed echo   
An echo is the audible leak-through of your own voice into your own receive (return) path.  
<img width="442" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/35c841cc-147f-4778-82c8-14203a032757">  
<img width="453" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/cf34fc98-d4b4-41d3-beaa-561ae6823e34">  
Two basic characteristics of echo are as follows:  
•The louder the echo (echo amplitude), the more annoying it is.  
•The longer the round-trip delay (the "later" the echo), the more annoying it is.  

### Effect of QoS on Echo
QoS might improve end-to-end network delay for a given level of congestion—the shorter the delay, the less annoying a given echo becomes.   
However, you will never be able to reduce the delay below the "danger zone" (25 ms) for echo perception with any form of QoS because the minimum delay inherent in VoIP networks is long enough for echos to be perceptible.   
QoS can help in other ways (for example, packet loss and jitter), but it cannot, by itself, eliminate echo.  



## GSM (-Erlang-B model) (2G)
`The GSM protocol is based on both TDMA and FDMA? Explain what that mean?`


### TDMA(Time Division Medium Access)

### FDMA(Frequency Division Medium Access)
## High Speed Circuit Switched Data (multi-rate model)


## GPRS(General Packet Radio Service)(2.5G)
`what are the main differences between GSM and GPRS from a performance point of view？`

## 802.11 Wireless LANs(Bianchi model)

### DCF（Distributed Coordination Function）
#### CSMA/CA
<img width="345" alt="image" src="https://github.com/zhang-mickey/network/assets/145342600/e630a030-0333-4b40-bb07-763de74214c1">

##### DIFS(Distributed Inter-Frame Spacing)
##### SIFS(Short Inter-Frame Spacing)
##### Contention window
##### Backoff

#### RTS/CTS handshaking
implementing RTS/CTS is to minimize collisions


## (Universal Mobile Telecommunication System) UMTS (3G)
### CDMA (code Division Medium Access)


# Literature
High Performance Browser Networking, Ilya Grigorik, O-Reilly, 2013.  
quene theory : https://www.cse.wustl.edu/~jain/queue/index.html  
Echo Analysis for Voice over IP: https://www.cisco.com/c/en/us/td/docs/ios/solutions_docs/voip_solutions/EA_ISD.html
