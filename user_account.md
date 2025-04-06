### User Account - State Diagram
```mermaid
stateDiagram-v2
    [*] --> Registered
    Registered --> Active: Email verified
    Active --> Suspended: Reported or policy violation
    Suspended --> Reactivated: Admin clears status
    Reactivated --> Active
    Active --> [*]
```
**Explanation:** Aligns with FR-001 (User registration and authentication), and US-001 (As a user, I want to register and log in).