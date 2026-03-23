# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types



## AIM:

To implement Abstract Factory Pattern for creating UI components based on theme.


## ALGORITHM :

1.Create interfaces for Button and Checkbox

2.Implement Dark and Light variants

3.Create UIFactory interface

4.Implement factory classes for each theme

5.Read theme input

6.Create corresponding factory object

7.Generate and display components




## PROGRAM:
 ```

Program to implement a Abstract Factory Pattern using Java
Developed by: Raha Priya Dharshini M
RegisterNumber: 212224240124
import java.util.Scanner;

interface Button { void render(); }
interface Checkbox { void render(); }

class DarkButton implements Button {
    public void render() { System.out.println("Dark Button created"); }
}
class LightButton implements Button {
    public void render() { System.out.println("Light Button created"); }
}
class DarkCheckbox implements Checkbox {
    public void render() { System.out.println("Dark Checkbox created"); }
}
class LightCheckbox implements Checkbox {
    public void render() { System.out.println("Light Checkbox created"); }
}

interface UIFactory {
    Button createButton();
    Checkbox createCheckbox();
}

class DarkThemeFactory implements UIFactory {
    public Button createButton() { return new DarkButton(); }
    public Checkbox createCheckbox() { return new DarkCheckbox(); }
}

class LightThemeFactory implements UIFactory {
    public Button createButton() { return new LightButton(); }
    public Checkbox createCheckbox() { return new LightCheckbox(); }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String theme = scanner.nextLine().toLowerCase();
        UIFactory factory;
        if (theme.equals("dark")) factory = new DarkThemeFactory();
        else if (theme.equals("light")) factory = new LightThemeFactory();
        else {
            System.out.println("Invalid theme");
            return;
        }
        factory.createButton().render();
        factory.createCheckbox().render();
    }
}

```



## OUTPUT:

<img width="1270" height="307" alt="image" src="https://github.com/user-attachments/assets/a84049eb-c467-4d82-b331-c6ff029f5157" />




## RESULT:
The program successfully creates UI components based on the selected theme using Abstract Factory Pattern.
