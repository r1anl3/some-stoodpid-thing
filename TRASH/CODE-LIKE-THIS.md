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
- Quantity
    - A class should not has more than 500 lines.
   ```java
   Class UserInformation {
        // No more than 500 lines in this class
   }
   ```
   - A function should not reaches 30 lines, not contains more than 5 paremeters, do only 1 job.
  ```java
  void doSomethingHere(int PARA_NOT_HIGHER_5) {
        // Lowers than 30 lines here
        // Only doSomething
  }
  ```
    - A line length should not over 80
    ```java
    String myLine = "I am so long but my lenght will not longer than 80.
    If so, i will line break my seft like this";
    ```
    - A statement should not be nested more than 4 levels
   ```java
   String myName = ParentTree().getGrandParents().
                    .GetParents()
                    .GetMe()
                    .GetName();
   ```
- Comment:
    - Remove all unused code
    ```java
    doSomething();
    //doNothing() Delete me please!
    ```
    - Comment to clarify logic 
    ```java
    void doSomething() {
            // Adding coffee bean to the coffee maker
            iDontUnderStand();
            givetMeInformationAboutThis();
            helpMe();
    }
    ```
    - Comment to warning developer about cases that may appeared 
   ```java
   void makingCoffee(Object coffeeBean) {
        // Add coffee bean to coffee maker, serve me a delicious cup of coffee 
        try {
            // Add some bean and serve me
            addCoffeeBeanToCoffeeMaker();
            serveMe();
        }
        catch {
            // The coffee maker may not be plugged
            tellMeWhatsWrong();
        }
   }
   ```