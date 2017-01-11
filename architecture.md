## Architecture

### Interaction Styles

There are a number of different ways systems and applications can interact, with a multitude of fine-grained technical attributes that describe detailed behaviors and properties.

At the highest level we've chosen to use three basic interaction styles when describing architectural patterns:

* Real-Time
* Store and Forward
* Batch

#### Real-Time

A real-time interaction is one where all parties have a general expectation that something will happen "right now." "Right now" is a loose term, but in general it means that something will happen on the order of seconds or less rather than days or weeks. Real-time interactions are often (but not always) short exchanges involving events or data. We use the letter "R" to signify a real-time interaction.

#### Store and Forward

A store-and-forward interaction is one where the sending and receiving sides of an interaction may operate at different rates and a technical mechanism in-between them "smooths out" the interaction. The general expectation is that things sent by the sender will safely accumulate until the receiver is able to process them. The time delay between sender and receiver could be milliseconds, days, weeks or even years. Email messages are an example of store-and-forward behavior. We use the letter "F" to signify a store-and-forward interaction.

#### Batch

A batch interaction is one where groups of information elements are exchanged at the same time in "batches." A batch could be as small as one item or as large as billions of items, but the general idea is that some number of elements are collected together and transmitted as a group *without* the expectations of a real-time interaction. Batch interactions are often (but not always) larger exchanges involving collections of events or data. We use the letter "B" to signify a batch interaction.

### Architectural Patterns

Patterns are repeatable ways of organizing hardware, software and systems. They make it easier to recognize when a particular design goal can be implemented using a design that's been done before.

#### Pattern #1 - Produce and Consume Sensor Data via MQTT

![](https://replicablesmartcities.github.io/pattern1.svg)

<br>
<br>

---
[Home](https://replicablesmartcities.github.io)
