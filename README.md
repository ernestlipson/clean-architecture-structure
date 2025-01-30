# clean-architecture-structure
# CORE LAYER
This layer holds all the essential business logic and follows a crucial rule: it should not rely on any external libraries or dependencies, whether they're developed internally or externally. The only allowed dependency here is the programming language itself (in our case, Kotlin). No implementations should reside in the core layer, only interfaces for injection. Changes in clean architecture should only propagate from the inner layers to the outer layers, not the other way around. A change in the infrastructure layer should never trigger a change in the core layer.
# DOMAIN LAYER
This module houses the data classes, encompassing both the write and read models. However, it's also possible to have only the write model in this module and define the read model at the controller level (in the configuration layer). In such cases, you can map the read model using presenters.
# USE CASES
UseCase classes encapsulate the core business logic and can be aligned with the concept of "commands" in domain-driven design. By making the business logic independent of infrastructure and dependencies, we ensure its resilience over time.
Before you begin developing your application, you must first design the appropriate architecture.
When designing your application architecture, it is essential that you respond to several principles, including:

SOLID: five object-oriented programming principles contribute to the readability, adaptability, and maintainability of OOP designs.

KISS: a design principle stating that designs and/or systems should be as simple as possible in order to maximize user acceptance and interaction.

DRY: a software development principle which stands for 'don't repeat yourself,' that aims to reduce code duplication in favor of abstractions and avoiding redundancy.
Hexagonal Architecture: the Ports and Adapters architecture is based on the idea of separating the application into loosely coupled components in order to isolate the core business logic from outside concerns.

Onion Architecture: this architecture is made up of multiple concentric layers that connect to the core, which represents the domain. In fact, this architecture is based on the principle of control inversion.

The Clean architecture: Uncle Bob's architecture is based on the dependency inversion principle to define boundaries between high-level and low-level components. Furthermore, this architecture attempts to combine all previous architectures into a single actionable idea.
the fundamental objective of all these architectures is to achieve a clear separation of concerns.
<img src="https://github.com/user-attachments/assets/c33806bb-5e7d-4e59-9b17-b79b54a93d82" width="400" /> <img src="https://github.com/user-attachments/assets/c33806bb-5e7d-4e59-9b17-b79b54a93d82" width="400" />


