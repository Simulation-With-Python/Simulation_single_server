# Simulation_With_Python


## Introduction

A queue is a line of people or things to be handled in a sequential order. It is a sequence of objects that are waiting to be processed. Queuing theory is the study of queues for managing process and objects. Simulation has been applied successfully for modeling small and large complex systems and understanding queuing behavior. Analysis of the models helps to increases the performance of the system.Simulation helps in understanding the behaviour of a queuing system and also obtain certain very useful parameters. 

## Motivation

Currently there is a lot of demand for simulation. From that demand new simulating ideas and processes are being built. To take these ideas or processes further, we have created a simlation of a banking system that solves problem in a completely new way, in an easy way. And we have exposed the issue. While this is not the best solution, it is the first step in sloving the problem. Inspiration to work in future.


## Queing onceptions

A Queue has to be maintained well to synchronize between the average waiting time and the idle time of server. A queuing model in which input, computation,transmission, storage and output are discrete in time field, is called discrete queuing model. Inreal life, a queue can be imagined as though to be of some people waiting in bank, usage of Atm machines or cash counter phenomenon.

## About this Project

In this project, we are trying to simulate a single-server banking system. We have used Poisson and Exponential distribution for some random variables to generate interarrival time and service time respectively. Simulating 20 customers so far.

## Procedure

  -Now, we have to consider a single server to simulate the bank system.

  - We have to initial inter-arrival time and service time first.

  - Consider poison as inter-arrival time and exponential as service time generate 20 random values.

  - The generate arrival time, time service end, time service begins, waiting time, time spends in system & idle time step by step.

  - The value-generating equations are given in the code section.

  - The single-channel queuing model can be fitted in situations where the following seven conditions are fulfilled:

  - The number of arrivals per unit of time is described by poisson distribution. The mean arrival rate is denoted by λ.

  - The service time has exponential distribution. The average service rate is denoted by μ.

  - Arrivals are from an infinite population.

  - The queue discipline is FIFO, that is, the customers are served on a first come first serve basis.

  - There is only a single service station.

  - The mean arrival rate is less than the mean service rate.

  - The waiting space available for customers in the queue is infinite.

## Quick Links
1. https://towardsdatascience.com/simulating-a-queuing-system-in-python-8a7d1151d485
2. Probability distribution. (https://www.datacamp.com/community/tutorials/probability-distributions-python?fbclid=IwAR1Van10TbSh-pfjCA_zS5F3AXI8fmWGrSgNZ0QdUwm-NwZG6Aacqd-qHOg)
3. A short research. (https://morioh.com/p/2a0717880c2d)
4. https://towardsdatascience.com/simulating-a-queuing-system-in-python-8a7d1151d485

## Team Members

* Md Shahadat Islam. (https://github.com/Shahadat-shuvo),(https://www.facebook.com/shahadatislam.shuvo.7/)
* Md Ashraf Udin.(https://github.com/Ashrafud)
* Thirtha Das.(https://github.com/thirtha741)
* Ishrat Ishita.(https://github.com/ishratishita)


**Lets first try and visualize the system

![banking_simulate](https://user-images.githubusercontent.com/79735371/112964586-47accd00-916a-11eb-884d-778e422866cf.png)


1. ***State Variables:*** describe the system at a particular time
2. ***Simulation Clock:*** Keeps track of time
3. ***Statistical Counters:*** Variables for storing statistical info about performance parameters
4. ***Initialization Routine:*** A subprogram or class that initializes the model at time 0
5. ***Timing Routine:*** A subprogram or a class that determines the next event
6. ***Event Routine:*** A subprogram or a class that updates the system when a particular event occurs

## Timing Routine

The timing routine decides which event occurs next by comparing the scheduled time of events and advances the simulation clock to the respective event. Initially, the departure events are scheduled to occur at time infinity(since there are no customers), which guarantees that the first event will be an arrival event.

## Exponential Distribution

The exponential distribution describes the time between events in a Poisson point process, i.e., a process in which events occur continuously and independently at a constant average rate. It has a parameter λ called rate parameter, and its equation is described as :
![eqn](https://user-images.githubusercontent.com/79735371/112974967-e6d6c200-9174-11eb-88f6-835225005010.png)

A decreasing exponential distribution looks like :

![graph](https://user-images.githubusercontent.com/79735371/112975005-f3f3b100-9174-11eb-9296-a9f50b34cc21.png)

## Poisson Distribution
Poisson random variable is typically used to model the number of times an event happened in a time interval. For example, the number of users visited on a website in an interval can be thought of a Poisson process. Poisson distribution is described in terms of the rate (μ) at which the events happen. An event can occur 0, 1, 2, … times in an interval. The average number of events in an interval is designated λ (lambda). Lambda is the event rate, also called the rate parameter. The probability of observing k events in an interval is given by the equation:

![eqn1](https://user-images.githubusercontent.com/79735371/112975022-fbb35580-9174-11eb-925e-3660d943faaa.png)

The following figure shows a typical poisson distribution:

![graph1](https://user-images.githubusercontent.com/79735371/112975047-02da6380-9175-11eb-9b61-6d5e0bc9f446.png)


## Implementation Section

**Generate Arrivale & Service Time

Using ***Poisson*** & ***Exponential distribution*** we generating the random values which are define as arrival time & service time

![time routine](https://user-images.githubusercontent.com/79735371/112966447-10d7b680-916c-11eb-9789-f26017441012.png)




**Running the Simulation

The next step is to run the simulation. I decided to run it for 20 customers. I have used a **for loop** which updates the random number seed every time, runs for 20 times, and appends the results to a pandas **data frame**. Later this data frame is exported as an **tabulate form.

![tsb](https://user-images.githubusercontent.com/79735371/112969661-47630080-916f-11eb-9b8f-932cb368e7a4.png)
![wt](https://user-images.githubusercontent.com/79735371/112969682-4e8a0e80-916f-11eb-99de-3422267f4aa4.png)

## RESULT

Here is a snippet of the results obtained from 20 customers.


![table1 1](https://user-images.githubusercontent.com/79735371/113620992-e52d6280-967c-11eb-8cc6-6f761135fa7c.png)




## Conclusion

Simulation can be used as a crucial decision-making tool in many industries, from manufacturing to service and even biology. This project is just a small example of the endless possibilities of simulation. There are many Softwares and resources out there to model complex systems and simulate them with ease. However, the goal of this project was to get a fundamental understanding of how a discrete event simulation works and its use as a decision-making tool.
