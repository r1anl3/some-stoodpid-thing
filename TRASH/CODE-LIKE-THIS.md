# CODING CONVENTION
- Naming
    - Camel case: 
    ```java
    String firsName, lastName;

    String getMyName(String firstName, String lastName) {
        return firstName + lastName;
    }
   ```
    - Pascal case:
    ```java
    Class UserInformation {
        private static String FirstName, LastName;
    }
    ```
    - Snake case:
   ```java
    Class UserInformation {
        private static String FirstName, LastName;
        private static String USER_ID = "USER_ID";
    }
   ```
- Length
    - A class should not have more than 500 lines.
    - 