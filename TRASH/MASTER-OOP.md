# Object Oriented Programming
## *4 pilars*
- Abstract: trừu tượng hóa, mô hình hóa
    - Class: prototype, khuôn mẫu
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

## *S.O.L.I.D*
- Make code more readable.
- Stand for:
    - Single Resposibility: 
      - Mỗi class chỉ làm đúng việc của nó.
      - Chia thành nhiều class (micro services).

      ```mermaid
      flowchart LR
      user("User")
      service1("PostService")
      service2("FriendService")
      service3("MessageService")
      user --> service1
      user --> service2
      user --> service3
      ```
    - Open-Closed: open for **extension** but close for **modification**
      - Use ***Decorator Design Patten***
      ```Java
      public class A implements FeatureInterface {
            public void doSomething() {
                  // Your code here
            }
      }
      ```
      ```Java
      public class B implements FeatureInterface {
            protected FeatureInterface a;
            protected B(FeatureInterface a) {
                  this.a = a;
            }

            public void doSomething() {
                  this.a.doSomething();
            }
      }
      ```
      - Dependency Injection: trong runtime, có thể chọn khi nào dùng **class A**, khi nào dùng **class B**
    - Liskov Substituition: 
      - Class con có khả năng thay thể được class cha.
      - Không làm mất đi tính đúng.

      ```mermaid
      classDiagram
            SavingAccount <|-- WithdrawableAccount
            SavingAccount <|-- NonWithdrawableAccount
            SavingAccount: +withDraw(amt)

            class WithdrawableAccount{
                  +withDraw(amt)
            }
            class NonWithdrawableAccount{
                  +deposit(amt)
            }

            WithdrawableAccount  <|-- GeneralAccount
            class GeneralAccount{
                  +withDraw(amt)
            }

            NonWithdrawableAccount  <|-- KidsAccount
            class KidsAccount{
                  +withDraw(amt)
            }
      ```