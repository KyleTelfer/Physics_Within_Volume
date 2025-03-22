# Facility and Machine Concepts

This directory contains documentation and notation for facility and machine workflows within the **Volume Interaction Framework**. Each file describes a specific facility or machine concept, including its components, connections, and workflow notation.

The goal of these documents is to provide a modular and intuitive way to design and analyze facilities and machines using the principles of **volume interactions**, **degradation factors**, and **observer-dependent measurements**.

---

## Table of Contents

1. [Overview of Facility Workflow Notation](#overview-of-facility-workflow-notation)
2. [Facility Components or Units](#facility-components-or-units)
3. [Types of Connections](#types-of-connections)
4. [Component or Unit Connections](#component-or-unit-connections)
5. [Example Facility](#example-facility)
6. [Contributing](#contributing)

---

## Overview of Facility Workflow Notation

Facility workflows are represented using a **skeleton notation** that describes the components, connections, and modular entry/exit points of a facility or machine. This notation is designed to be flexible and scalable, allowing for the representation of complex systems while respecting computational limits.

Key elements of the notation include:
- **Facility Name and Description**: A brief overview of the facility or machine concept.
- **Components or Units**: Each unit in the facility is assigned a number and a name.
- **Types of Connections**: The connections between units are categorized by type and assigned a number.
- **Workflow Notation**: The flow of materials or processes through the facility is represented using a combination of dashes, question marks, and connection types.

---

## Facility Components or Units

Each facility or machine is composed of **units**, which are the individual components that perform specific functions. Each unit is assigned:
- A **number** (e.g., `2.1`, `2.2`) for easy reference.
- A **name** that describes its function (e.g., `Intake`, `Submerged Shredder`).

---

## Types of Connections

Connections between units are categorized by **type**, which describes the nature of the interaction between components. Each connection type is assigned a number in parentheses (e.g., `(3.1)`, `(3.2)`). The types of connections include:
- **3.1**: Centripetal Separation
- **3.2**: Auger
- **3.3**: Conveyor
- **3.4**: Magnetic
- **3.5**: Vacuum
- **3..**: Placeholder for undefined connection types.

---

## Component or Unit Connections

The workflow notation describes how units are connected and how materials or processes flow through the facility. Key rules for notation include:
- **Modular Entry Points**: Represented by `-?` at the start of a workflow.
- **Modular Exit Points**: Represented by `-?-` at the end of a workflow.
- **Connection Types**: Represented by numbers in parentheses between dashes (e.g., `- (3.1) -`).
- **No Loops**: Modular entry points cannot link to earlier points in the workflow to avoid loops.

### Example Workflow Notation

2.1 -?
-? (3..) - 2.2 -? 
-? (3..) - 2.3 - (3..) - 2.6 -?-
-? (3..) - 2.4 - (3..) - 2.2 -?
-? (3..) - 2.4 - (3..) - 2.6 -?-
-? (3..) - 2.6 -?
-? (3..) - 2.6 -?-

Example Facility
1.1 Waste Facility
A community waste management concept.

2.1 Intake
The entry point for waste materials.

2.2 Submerged Shredder
A unit that shreds waste materials in a liquid medium.

2.3 Waste Transport (Light Density)
Transports waste that is not processed by the shredder.

2.4 Waste Transport (Heavy Density)
Transports waste that is processed by the shredder.

2.5 Liquid Density Medium Management
Manages the liquid medium used in the shredding process.

2.6 Packing and Shipping
Prepares processed waste for shipment.

Contributing
Contributions to this directory are welcome! If you have suggestions for improving the notation or want to add new facility or machine concepts, please:

Fork the repository.

Create a new branch for your changes.

Submit a pull request with a detailed description of your contributions.

License
This work is licensed under the MIT License.
