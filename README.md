# Cheatsheet-Java

Type de données, primitives :
```java
char
byte
short
int
long
float
double
boolean
```

Classe de base :
```java
String
```

Constantes exemples :
```java
final int NUMBEROFWEEKDAYS = 7;
final String MYFAVOURITEFOOD = "Icecream";
NUMBEROFWEEKDAYS = UMBEROFWEEKDAYS + 1; // Erreur
MYFAVOURITEFOOD = "Cake"; // Erreur
```

Étapes pour créer cette fonction :
Créer un dossier, ce qu'on appelle généralement le dossier root, créez un dossier "hello", créez un fichier HelloWorld.java.

Fonction :
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}
```

Fonction plus propre :
```java
public class CleanWorld {
   public static void main(String[] args) {
      sayHelloTo("world");
   }

   /** affiche le message "hello" au destinataire fourni
   *
   * @param recipient
   */
   private static void sayHelloTo(String recipient) {
      System.out.println("Hello " + recipient);
   }  
}
```

Niveaux de contrôle :

    public : visible pour tous et par conséquent le moins restrictif

    protected : visible pour le package et l'ensemble de ses sous-classes

    package-protected : généralement visible uniquement par le package dans lequel il se trouve (paramètres par défaut). Ne pas mettre de mot clé déclenche ce niveau de contrôle

    private : accessible uniquement dans le contexte dans lequel les variables sont définies (à l'intérieur de la classe dans laquelle il est situé).

```java
class PrivateClass {
    int internalProperty = 0; // assigne automatiquement package-private par défaut
    protected defaultProperty = true; // assigne automatiquement package-private
    public boolean publicProperty = true; // convertit automatiquement en package-private
    private String fileprivateProperty = "Hello!"; //disponible seulement pour la classe
    private static void privateMethod() {
    }
    PrivateClass a = new PrivateClass(); // Erreur
    private PrivateClass b = new PrivateClass(); // Ok
    private PrivateClass c = new PrivateClass(); // Ok
}
```

Loops :
```java
int[] myArray = new int[]{7,2,4};
for (int i=0; i<myArray.length; i++) {
    System.out.println(myArray[i]);
}

int numberOfTrees = 0;
while (numberOfTrees < 10) {
   numberOfTrees += 1;
   System.out.println("I planted " + numberOfTrees + " trees");
}

System.out.println("I have a forest!");

int pushUpGoal = 10;
do{
   print ("Push up!");
   pushUpGoal -= 1;
} while(pushUpGoal > 0);
```

Comparaison strings :
```java
String weatherToday="The weather is good";
String weatherTomorrow="The weather is good";
weatherToday.equals(weatherTomorrow); // -> true
```
Switch :
```java
public static void main(String[] args) {
    switch(args.length) {
        case 0: // aucun argument n'a été envoyé
            sayHelloTo("world");
            break;
        case 1: // l'utilisateur a fourni un argument dans le terminal
            sayHelloTo(args[0]);
            break;
        case 2: // l'utilisateur a fourni 2 arguments
            sayHelloTo(args[0] + "-" + args[1]);
            break;
        default: // l'utilisateur a fourni plus d'arguments qu'on peut en gérer !
            System.out.println("Sorry, I don't know how to manage more than 2 names!");
    }
}
```