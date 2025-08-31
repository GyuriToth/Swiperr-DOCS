# Design and Development Guideline

When developing any complex project — whether hardware, software, or a combination — it’s crucial to distinguish between **requirements**, **system design**, **architecture design**, and **model design**.
These stages build upon each other, moving from abstract needs to concrete implementation details.

Understanding Requirements, System Design, Architecture Design, and Model Design

---

## 1. Requirements — *Defining “What” the System Must Do*
**Purpose:**
Requirements capture the **functional** and **non-functional** needs of the system, describing *what* it must achieve without dictating *how* it will be built.

**Key Points:**
- Written in user-oriented language.
- Should be testable and measurable.
- Serve as the foundation for all later design work.

**Example (Autonomous Delivery Robot):**
- Must deliver packages within a 5 km radius in under 30 minutes.
- Must avoid pedestrians and obstacles.
- Must operate for at least 8 hours on a single charge.

---

## 2. System Design — *Defining the Major Components*
**Purpose:**
System design breaks the system into **high-level functional blocks** and defines their roles.
It is the stage where we decide *what subsystems exist* and *what each does*.

**Key Points:**
- Focuses on *what parts* the system will have.
- Components are described broadly, not yet in detail.
- Often documented as block diagrams.

**Example (Autonomous Delivery Robot):**
- Navigation subsystem (GPS, mapping, path planning).
- Locomotion subsystem (motors, wheels, suspension).
- Perception subsystem (cameras, LIDAR, ultrasonic sensors).
- Communication subsystem (4G/5G module, cloud interface).
- Power subsystem (battery, charging circuit).

---

## 3. Architecture Design — *Defining How Components Work Together*
**Purpose:**
Architecture design specifies **how the system’s components interact**, both physically and logically.
This is where design patterns, control flow, and communication structures are chosen.

**Key Points:**
- Defines **relationships**, **interfaces**, and **data flow**.
- May include technology selection (e.g., microservices vs. monolith, centralized vs. distributed control).
- Serves as the blueprint for developers and engineers.

**Example (Autonomous Delivery Robot):**
- Sensors feed raw data to the perception module → processed into a world map → passed to path planning.
- Navigation outputs control commands to motor controllers.
- Communication module exchanges delivery status with a cloud server.
- Power management module monitors battery and triggers return-to-base when low.

---

## 4. Model Design — *Detailed Representations for Implementation*
**Purpose:**
Model design develops **precise, implementable representations** of individual system parts.
This includes algorithms, mathematical models, physical CAD designs, and data schemas.

**Key Points:**
- This is the most detailed stage before actual coding or building.
- Models can be analytical (formulas, simulations) or physical (CAD, schematics).
- Supports testing and validation before full implementation.

**Example (Autonomous Delivery Robot):**
- Navigation model: Kalman filter equations for GPS + IMU fusion.
- Obstacle detection model: Convolutional neural network trained on pedestrian datasets.
- Battery usage model: Mathematical curve for discharge under load.
- 3D CAD models of chassis and suspension for stress analysis.

---

## Hierarchy Summary

| Stage                 | Focus Question        | Level of Detail   | Example Output |
|-----------------------|----------------------|------------------|----------------|
| **Requirements**      | What must it do?     | Abstract         | List of capabilities, performance targets |
| **System Design**     | What are the parts?  | High-level       | Block diagrams, subsystem descriptions |
| **Architecture Design** | How do the parts interact? | Mid-level       | Interface specs, communication flow |
| **Model Design**      | What is the exact form/algorithm? | Detailed        | CAD files, mathematical models, ML architectures |

---

**Best Practice Tip:**
Always validate each stage before moving on.
If the requirements are unclear, the system design will be wrong.
If the system design is wrong, the architecture will be inefficient.
If the architecture is flawed, the models will be costly to redo.





## Testing

Every testable module or requirement shall have a corresponding test.
Tests must be writen in the same time as the module or requirements.


## Coding guideline
TODO: lit





## Definition of done
All tests pass. (Has at least 1 test)
The code is reviewed by 2 people.
*The code does what the requirements states.*


## Development Flow
*  Requirements - What features we want
*  System design - Basicly what we do to achive the features, application design, webdesign, and interaction of modules
*  Architecture design - How and what products conceoppts are we gona use
*  Module design - What objects and functions are we gona use
*  Coding phase - and test writing phase
*  Unit test - automated
*  Integration test - integrated
*  Integration - 2 eyes
*  System Test - automatation
*  System Deployment - automatation
*  Acceptance test - not implemented