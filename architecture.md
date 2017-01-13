## Architecture

### Interaction Styles

There are a number of different ways systems and applications can interact, with a multitude of fine-grained technical attributes that describe detailed behaviors and properties.

At the highest level we've chosen to use three basic interaction styles when describing architectural patterns:

* Real-Time
* Store and Forward
* Batch

The choice of a small number of easily understood interaction styles facilitates communication among the business and technical members of the team as well as across teams having different levels of technical depth.

#### Real-Time

A real-time interaction is one where all parties have a general expectation that something will happen "right now." "Right now" is a loose term, but in general it means that something will happen on the order of seconds or less rather than days or weeks. Real-time interactions are often (but not always) short exchanges involving events or data. We use the letter "R" to signify a real-time interaction.

#### Store and Forward

A store-and-forward interaction is one where the sending and receiving sides of an interaction may operate at different rates and a technical mechanism in-between them "smooths out" the interaction. The general expectation is that things sent by the sender will safely accumulate until the receiver is able to process them. The time delay between sender and receiver could be milliseconds, days, weeks or even years. Email messages are an example of store-and-forward behavior. We use the letter "F" to signify a store-and-forward interaction.

#### Batch

A batch interaction is one where groups of information elements are exchanged at the same time in "batches." A batch could be as small as one item or as large as billions of items, but the general idea is that some number of elements are collected together and transmitted as a group *without* the expectations of a real-time interaction. Batch interactions are often (but not always) larger exchanges involving collections of events or data. We use the letter "B" to signify a batch interaction.

### Architectural Patterns

Patterns are repeatable ways of organizing hardware, software and systems. They make it easier to recognize when a particular design goal can be implemented using a design that's been implemented before. There are many options, variations and details associated with any given technical architecture and we aren't attempting to describe every permutation. Instead, our aim is to describe the primary patterns that can be used to quickly differentiate, characterize and communicate how a particular replicable implementation works at the conceptual level.

---

#### Pattern #1 - Produce and Consume Sensor Data via MQTT

This pattern is used by sensors and applications that can communicate over a private or public network in real-time. It is typically used with sensors that periodically report information that other applications use. Devices and applications may be directly connected to the network or may communicate through a specialized communications network such as a mesh or point-to-point wireless network.

![](https://replicablesmartcities.github.io/pattern1.svg)

---

#### Pattern #2 - Send Message to Sensor via MQTT

This pattern is used by sensors and applications that can communicate over a private or public network in real-time. It is typically used to send commands or data to sensors from one or more controlling applications. Devices and applications may be directly connected to the network or may communicate through a specialized communications network such as a mesh or point-to-point wireless network. 

![](https://replicablesmartcities.github.io/pattern2.svg)

<br>
<br>

---
[Home](https://replicablesmartcities.github.io)
