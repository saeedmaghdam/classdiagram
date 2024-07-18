# Class diagram relations

## Overview

![](./relation/relations-in-uml-overview.png)

## Association

- **Description:** This represents a relationship between two classes that need to communicate with each other.
- **Example:** A **Teacher** teaches a **Student**.

```plantuml
@startuml
class Teacher
class Student

Teacher --> Student : teaches
@enduml
```

![](./relation/association.png)

## Aggregation

- **Description:** This is a special form of association that represents a "whole-part" relationship but with weaker bonds. The part can exist independently of the whole.
- **Example:** A **Library** contains **Books**, but a **Book** can exist without the **Library**.

```plantuml
@startuml
class Library
class Book

Library o-- Book : contains
@enduml
```

![](./relation/aggregation.png)

## Composition

- **Description:** This is a stronger form of aggregation where the part cannot exist without the whole. If the whole is destroyed, the parts are too.
- **Example:** A **House** has **Rooms**. If the **House** is destroyed, the **Rooms** are too.

```plantuml
@startuml
class House
class Room

House *-- Room : has
@enduml
```

![](./relation/composition.png)

## Inheritance (Generalization)

- **Description:** This represents an "is-a" relationship. A child class inherits attributes and methods from a parent class.
- **Example:** A **Dog** is an **Animal**.

![](./relation/generalization.png)

## Realization

- **Description:** This relationship is used to show that a class implements an interface.
- **Example:** A **Printer** implements a **Printable** interface.

```plantuml
@startuml
interface Printable
class Printer

Printable <|.. Printer : implements
@enduml
```

![](./relation/realization.png)

## Full Example

```plantuml
@startuml
class Teacher
class Student
class Library
class Book
class House
class Room
class Animal
class Dog
interface Printable
class Printer

Teacher --> Student : teaches
Library o-- Book : contains
House *-- Room : has
Animal <|-- Dog : is-a
Printable <|.. Printer : implements
@enduml
```

![](./relation/fullexample.png)

## Referrences
- [https://www.umlboard.com/docs/relations/](https://www.umlboard.com/docs/relations/)