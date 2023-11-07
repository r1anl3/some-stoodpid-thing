# Object Oriented Programming
## *4 pilars*
- Abstract: trừu tượng hóa, mô hình hóa.
      - Class: prototype, khuôn mẫu.
      - Object: thực thể
- Encapsulation: đóng gói
      - Access modifier: private, public, protected
      - Field, method
      - Cho thấy thứ cần thấy
- Inheritance: kế thừa

```mermaid
classDiagram
      Person <|-- Developer
      Person <|-- Manager
      Person <|-- Designer
      Person: +String name
      Person: +age int
      Person: +dob Datetime
      Person: +goToWork()
```

- Polymophism: đa hình  
      - Overwrite các function

```mermaid
classDiagram
      Person <|-- Developer
      Person <|-- Manager
      Person <|-- Designer
      Person: +String name
      Person: +age int
      Person: +dob Datetime
      Person: +goToWork()
      class Developer{
            inherited from Person
            gotowork() coding
      }
      class Manager{
            inherited from Person
            gotowork() managing
      }
      class Designer{
            inherited from Person
            gotowork() designing
      }
```