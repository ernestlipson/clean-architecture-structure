# clean-architecture-structure
# CORE LAYER
This layer holds all the essential business logic and follows a crucial rule: it should not rely on any external libraries or dependencies, whether they're developed internally or externally. The only allowed dependency here is the programming language itself (in our case, Kotlin). No implementations should reside in the core layer, only interfaces for injection. Changes in clean architecture should only propagate from the inner layers to the outer layers, not the other way around. A change in the infrastructure layer should never trigger a change in the core layer.
# DOMAIN LAYER
This module houses the data classes, encompassing both the write and read models. However, it's also possible to have only the write model in this module and define the read model at the controller level (in the configuration layer). In such cases, you can map the read model using presenters.
# USE CASES
UseCase classes encapsulate the core business logic and can be aligned with the concept of "commands" in domain-driven design. By making the business logic independent of infrastructure and dependencies, we ensure its resilience over time
