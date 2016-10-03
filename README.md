# mic-webgme
## Installation
First, install the mic-webgme following:
- [NodeJS](https://nodejs.org/en/) (v4.x.x recommended)
- [MongoDB](https://www.mongodb.com/)

Second, start mongodb locally by running the `mongod` executable in your mongodb installation (you may need to create a `data` directory or set `--dbpath`).

Then, run `webgme start` from the project root to start . Finally, navigate to `http://localhost:8888` to start using mic-webgme!

# Passive Electrical Circuits

## Target Audience
The target audience for this modeling language would be electrical engineers who would like to model connecting together passive electrical circuits (resistors, capacitors, and inductors).

## Metamodel
The metamodel defines an Example Models node which holds many Circuits. The Circuits may contain additional Circuits, nodes of type ComponentsBase, and PortConnection transitions. ComponentsBase is an abstract node with children Resistor, Capacitor, and Inductor. ComponentsBase and its children may contain any number of Input and Output (Input and Output of which are children of the abstract node PortBase). PortConnection is an abstract node with child Output2Input. Output2Input is a transition with source Output and destination Input.

Resistor, Capacitor, and Inductor have been defined as containing one Input and one Output. Resistor has an attribute called "resistance" which is a float. Capacitor has an attribute called "capacitance" which is a float. Inductor has an attribute called "inductance" which is a float.

## Example Models
The example models are three circuits. One contains connecting a Resistor output to an Inductor input then Inductor output to a Capacitor input then Capacitor output Resistor input. Another circuit contains two Resistors connected to an Inductor. The last circuit contains a Resistor connected to two Inductors.
