---
layout: post
title: pop、propagation delay和transmission delay
categories: 学术
description: 论文阅读过程中总结的网络知识
keywords: pop, propagation delay
---

## 计算机网络知识-pop、propagation delay和transmission delay

* **pop**

  POP入网点(point-of-presence)。对于企业来说，pop位于企业网络的边缘外侧，是外部用户访问企业内网的进入点，也是内部用户通往外部服务和站点的链路。对于ISP来说，pop是一个将互联网从一个地方接到其他地方的入网点，pop必须有一个全网唯一的IP地址。

***

* **propagation delay与transmission delay**

> [参考](http://blog.163.com/hair_communication/blog/static/20198911920123258334463/)

propagation delay，传播时延，指电磁信号/光信号在传输介质中传播的时延。

transmission delay，发送时延，数据库从第一个比特发送算起，到最后一个比特发送完毕所需的时间。

bandwidth，带宽，媒体接入速度，即数据从节点进入到媒体的速度。

比较：传播时延和要发送的数据大小没有关系，发送时延与发送数据的大小有关，发送时延=数据/带宽，传播时延=发送距离/传播速率。在光纤，双绞线，电缆等传输媒体中，传播速率是固定的。因此，传播时延主要是与传输距离有关！而与发送的数据大小无关！

*英文解释*

* Propagation delay is how long it takes *one* bit to *travel* from one end of the "wire" to the other (it's proportional to the length of the wire, crudely).

  Transmission delay is how long it takes to get *all* the bits *into* the wire in the first place (it's packet_length/data_rate).

* The transmission delay is the amount of time required for the router to push out the packet.

  The propagation delay is the time it takes a bit to propagate from one router to the next.

*详细介绍*

* transmission delay



     	In a network based on packet switching, transmission delay (or store-and-forward delay) is the amount of time required to push all of the packet's bits into the wire. In other words, this is the delay caused by the data-rate of the link.

    	Transmission delay is a function of the packet's length and has nothing to do with the distance between the two nodes. This delay is proportional to the packet's length in bits,It is given by the following formula:

    ​											DT = N / R 
    	where DT is the transmission delay, N is the number of bits, and R is the rate of transmission (say in bits per second). Most packet switched networks use store-and-forward transmission at the input of the link. A switch using store-and-forward transmission will receive (save) the entire packet to the buffer and check it for CRC errors or other problems before sending the first bit of the packet into the outbound link. Thus store-and-forward packet switches introduce a store-and-forward delay at the input to each link along the packet's route.

* propagation delay

  ​	The time required for a signal to pass through a given complete operating circuit; it is generally of the order of nanoseconds, and is of extreme importance in computer circuits. 

  ​	The time it takes to transmit a signal from one place to another. Propagation delay is dependent solely on distance and two thirds the speed of light. Signals going through a wire or fiber generally travel at two thirds the speed of light. 

  ​	Networking Propagation delay is defined as the amount of time it takes for a certain number of bytes to be transferred over a medium. Propagation delay is the distance between the two routers divided by the propagation speed.

  ​									Propagation delay = d/s

  ​	 where d is the distance and s is the speed.

  ​	In electronics, digital circuits and digital electronics, the propagation delay, or gate delay, is the length of time starting from when the input to a logic gate becomes stable and valid, to the time that the output of that logic gate is stable and valid. Often this refers to the time required for the output to reach 50% of its final output level when the input changes. Reducing gate delays in digital circuits allows them to process data at a faster rate and improve overall performance.

  ​	The difference in propagation delays of logic elements is the major contributor to glitches in asynchronous circuits as a result of race conditions.The principle of logical effort utilizes propagation delays to compare designs implementing the same logical statement.

  ***

  ​