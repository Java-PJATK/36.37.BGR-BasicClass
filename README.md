# BGR-BasicClass  

36 BGR-BasicClass/Person.java 67   
37 BGR-BasicClass/Main.java 68  

Cont. from 8.4 Constructors and methods [35.GBP-Point](https://github.com/Java-PJATK/35.BGP-Point)  

Another example  

## Listing 36 BGR-BasicClass/Person.java 67   
```java
public class Person {

    private String name;
    private int birth_year;

    public Person(String name, int r) {
        this.name = name;
        birth_year = r;
    }

    public String getName() {
        return name;
    }

    public int getYear() {
        return birth_year;
    }
    /**/
    @Override
    public String toString() {
        return name + " (b. " + birth_year + ")";
    }
    /**/

    public boolean isOlderThan(Person other) {
        return birth_year < other.birth_year;
    }
}
```

and the class `Main` which uses `Person`  

```java
// BGR-BasicClass/Main.java
 
import javax.swing.JOptionPane;

public class Main {
    public static void main(String[] args) {

        Person john = new Person("John", 1980);
        Person mary = new Person("Mary", 1985);

        System.out.println(
            "Two Persons created: " + john + " and " + mary);

        Person older = mary.isOlderThan(john) ? mary : john;
        System.out.println("Older: " + older.getName() +
                " born in " + older.getYear());

        String s = older + " is older";

        // JOptionPane.showMessageDialog(null,s);
        System.out.println(s);
        System.exit(0);
    }
}
```

The program prints  

```
Older: John born in 1980
John (b. 1980) is older
```
