
# Requirement Analysis, Specification and Design Document for electrical vehicle charging station software

This repo contains the Requirement Analysis and Specification Document, and Design Documents for the software system of electrical vehicle charging service. These documents were developed as a project during the "Software Engineering" 2022/23 A. Y. course at PoliMi. 

The objective of this project is to apply software engineering practices to address software engineering issues in a rigorous way and develop RASD and DD for eMall system described in the following section. The project includes two documents:

1. The **Requirement Analysis and Specification Document (RASD)** for the e-Mobility problem: contains the description of the scenarios, the use cases that describe them, and the models describing the requirements and specification for the problem under consideration. The description tools are natural language, UML, and Alloy.

2. The definition of the **Design Document (DD)** for the e-Mobility problem. Contains a functional description of the system, and any other useful views. UML diagrams are used to provide a full description of the system.

## Software system desription

Electric mobility (e-Mobility) is a way to limit the carbon footprint caused by our urban and sub-urban mobility needs. When using an electric vehicle, knowing where to charge the vehicle and carefully planning the charging process in such a way that it introduces minimal interference and constraints on our daily schedule is of paramount importance. 

e-Mobility Service Providers (eMSPs) offer to end users the possibility to:

1. know about the charging stations nearby, their cost, any special offer they have;
2. book a charge in a specific charging station for a certain timeframe;
3. start the charging process at a certain station;
4. notify the user when the charging process is finished;
5. pay for the obtained service.

Charging stations are owned and managed by Charging Point Operators (CPOs). Each CPO has its own IT infrastructure administrated through the so-called Charge Point Management System (CPMS). The CPMS handles the acquisition of energy from external (3rd party) Distribution System Operators (DSOs)and distribute it to the connected vehicles, making decisions, such as the amount of energy to be used for each connected vehicle. CPOs can dynamically decide from which DSO to acquire energy, for instance, depending on the current price and/or on the used mix of energy sources and, based on these, can dynamically decide the cost of a charging and set special offers. If batteries are available at the charging station, a CPO can also decide whether to store or not energy and whether to use the energy available in the batteries instead of acquiring it from DSOs. These decisions can be handled either manually by human operators or automatically by CPMSs.

CPOs offer the following main functions through their CPMSs:

1. know the location and “external” status of a charging station (number of charging sockets available, their type such as slow/fast/rapid, their cost, and, if all sockets of a certain type are occupied, the estimated amount of time until the first socket of that type is freed);

2. start charging a vehicle according to the amount of power supplied by the socket, and monitor the charging process to infer when the battery is full;

3. know the “internal” status of a charging station (amount of energy available in its batteries, if any, number of vehicles being charged and, for each charging vehicle, amount of power absorbed and time left to the end of the charge);

4. acquire by the DSOs information about the current price of energy;

5. decide from which DSO to acquire energy (if more than one is available);

6. dynamically decide where to get energy for charging (station battery, DSO, or a mix thereof according to availability and cost).

The interaction between the various providers (eMSPs, CPOs, and DSOs) occurs through uniform APIs. Thanks to this, an eMSP can interact with multiple CPOs and, on the other side, a CPO can interact with multiple eMSPs. Hence, users can exploit a large variety of charging options. Similarly, a CPO can interact with multiple DSOs and vice versa.

The eMSP proactively suggests the user to go and charge the vehicle, depending on the status of the battery, the schedule of the user (this assumes that the eMSP application can get access to the calendar of the user and his/her navigation system), the special offers made available by some CPOs, and the availability of charging slots at the identified stations.

### Examples of companies working in this business area

- [Ionity](https://ionity.eu/)

- [Enel X](https://www.enelx.com/n-a/en.html)

- [Becharge](https://www.bec.energy/en)

- [Fastned](https://fastnedcharging.com/en/)

- [Atlante](https://atlante.energy/)


### Interesting references

- [Platform for Electromobility. EV Charging: How to tap in the grid smartly?](https://www.platformelectromobility.eu/2022/05/17/ev-charging-how-to-tap-in-the-grid-smartly/) May 2022 

- [F. Campos, L. Marques, and K. Kotsalos, Electric Vehicle CPMS and Secondary Substation Management.](https://mobilityintegrationsymposium.org/wp-content/uploads/sites/10/2018/11/4A_3_Emob18_024_paper_Filipe_Campos.pdf) 2nd E-Mobility Power System Integration Symposium, Stockholm, Sweden, 15 October 2018. 

- Shu Su, Hui Yan, and Ning Ding. 2018. [Machine Learning-Based Charging Network Operation Service Platform Reservation Charging Service System.](https://doi.org/10.1145/3297067.3297078) In Proceedings of the 2018 International Conference on Signal Processing and Machine Learning (SPML '18). Association for Computing Machinery, New York, NY, USA, 1–5. 


