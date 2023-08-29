##Designing a database for an airlines company

##Summary

In this project, we designed an efficient and scalable database for an abstract airline company by considering the intricacies of the airline network. An ERD and Relational scheme have been provided below.

##Description

Airlines would have flights identified by an Airline number. Each flight has attributes like airline code, and days of the week the flight is operated( Operational_days).

Each flight has one or more legs identified as leg_id, a leg is a non-stop portion of a flight within the entire length of the operation. For a given flight, flight legs will be identified by sequence numbers. (Flight 1620 has leg 1 Seattle — Portland, and leg 2, Portland — Phoenix)

An actual occurrence of a flight is implemented as aleg instance. A leg instance is an instance of a flight leg. For a given flight leg, an instance is identified by the flight date. For each leg instance, number of available seats is kept track of.

An airplane is assigned to each leg instance. Airplanes are identified by plane ID. We also track additional attributes, like the total number of seats.

Each airplane belongs to an airplane type, identified by type name, with other attributes max seats, and manufacturer. Airports are identified by airport codes, with attributes like name, city, etc.

Each flight leg is scheduled to depart from an airport, with a scheduled departure time. Each flight leg is scheduled to arrive at an airport, with a scheduled arrival time.

Each leg instance departs from an airport, with an actual departure time, Each leg instance arrives at an airport, with an actual arrival time.

Each flight has multiple fares. A fare has a fare code, restrictions, and amount. The fare code may be common across multiple flights but will be unique for a given flight. A specific instance of a fare is associated with a specific flight. (Fare code being same for two different flights does not mean the same fare)

Corresponding to each leg instance, we also track each seat. For a given leg instance, the seat is identified by seat number, and we record the passenger name, phone number, origin, destination, baggage code, baggage count, and payment id. (The payment id is to refer to a different database that tracks reservations, payments, and so on)

