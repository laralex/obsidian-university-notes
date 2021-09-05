[[Controller|Controller]] and [[System|System]] communicate in a closed loop:
```mermaid
flowchart LR;
    Controller-->|Action|System;
    System-->|Response|Controller;
```