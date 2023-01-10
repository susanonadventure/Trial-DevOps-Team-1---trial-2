# Java 

Java ist eine objektorientierte und plattformübergreifende Programmiersprache für verschiedenen Betriebssysteme und Plattformen und eine eingetragene Marke des Unternehmens Oracle. 

Die Java-Programmen können auf jeder Art von Computer ausgeführt werden, solange dort eine Java-Laufzeitumgebung ("*Java Runtime Environment*" oder "*JRE*") installiert ist. 

Die Sprache wird häufig in großen Unternehmensanwendungen, auf Android-Smartphones und im Web verwendet.

## JDK (Java Development Kit)

Die JDK ist eine Sammlung von Werkzeugen zur Entwicklung von Java-Anwendungen. Die JDK enthält alle notwendigen Komponenten, um Java-Code zu schreiben, zu kompilieren und auszuführen.

![](jdk.drawio.png)

Die JDK enthält:

- Das Java-Compiler-Programm (javac), das verwendet wird, um Java-Code in Bytecode zu kompilieren.

- Das Java-Interpreter-Programm (java), das verwendet wird, um Java-Bytecode auszuführen.

- Bibliotheken und andere Unterstützungsdateien, die von Java-Anwendungen verwendet werden.

Um Java-Anwendungen zu entwickeln, müssen wir zunächst das JDK installieren. Die Installation kann im Terminal erfolgen:

```
sudo apt-get update
```
```
sudo apt-get install openjdk-17-jdk openjdk-17-demo openjdk-17-doc openjdk-17-jre-headless openjdk-17-source
```

[Für mehr Info über die Installation](https://wiki.ubuntuusers.de/Java/Installation/OpenJDK/)

Unter folgenden Befehlen können wir checken, ob die Installation erfolgreich gelaufen ist:

```
java -version
```
```
which javac
```
**NOTE** *Da wir VSCode als Code-Editor benutzen, brauchen wir noch das "Java Extention Pack" herunterzuladen.*

Teil der JDK ist auch die JVM (*Java Virtual machine*).Die JVM ist eine virtuelle Maschine, die die Java-Bytecode übersetzt und ausführt. Dies ermöglicht, dass Java-Anwendungen auf jedem Computer ausgeführt werden können, solange der Computer über die notwendigen Ressourcen verfügt.

## Java-Dateien

In Java gibt es verschiedene Arten von Dateien, die bei der Entwicklung von Java-Anwendungen verwendet werden:

- **.java-Dateien:** enthalten den Java-Sourcecode, die wir im Code-Editor schreiben. Jede .java-Datei enthält normalerweise eine oder mehrere Java-Klassen.

- **.class-Dateien:** Diese Dateien enthalten den Bytecode, der von der Java Virtual Machine (JVM) interpretiert und ausgeführt wird.

- **.jar-Dateien:** Diese Dateien sind Java Archive (JAR), die mehrere .class-Dateien und andere Ressourcen (wie z.B. Bilder und Klangdateien) enthalten können. JAR-Dateien werden oft verwendet, um Java-Anwendungen oder Bibliotheken zu verteilen.

- **.jdb-Dateien:** Diese Dateien sind Java Debugging Wire Protocol (JDWP)-Dateien, die von Java-Debugger-Tools verwendet werden, um Java-Anwendungen zu debuggern.

Es gibt auch andere Arten von Dateien, die bei der Entwicklung von Java-Anwendungen verwendet werden können, wie z.B. Manifest-Dateien und Property-Dateien.

## Variablen (Primitive Data Types)

In Java gibt es verschiedene Datentypen, die verwendet werden, um unterschiedliche Arten von Werten zu speichern. Die verfügbaren Datentypen sind in zwei Kategorien unterteilt: primitive Datentypen und referenzielle Datentypen.

Primitive Datentypen sind die grundlegenden Datentypen in Java, die direkt von der JVM unterstützt werden. Sie erden unter folgender Tabelle umgefasst:

![](data.png)

![](range.png)

Referenzielle Datentypen sind Variablen, die Verweise auf Objekte speichern, beispielsweise *Klassentypen* (von Benutzer definierte Klassen), *Interface-Typen* (von Benutzer definierte Interfaces) und 
*Array-Typen* (Arrays , die die gleichen Datentypen speichern).

Die Wahl des richtigen Datentyps hängt von der Art der Werte ab, die wir speichern möchten, von den Anforderungen an die Speichergröße und von der Genauigkeit (Integer oder Dezimal). 

Es ist wichtig, den passenden Datentyp zu verwenden, um die Leistung und die Genauigkeit des Programms zu optimieren.

## Das Hello-World-Programm in Java

```java
package com.bit.java_project //Strukturverzeichnis des Packages

pubblic class Hello-World{ //Class 
    pubblic static void main(string[]args){ // Main-Funktion
        System.out.println("Hello World");
    }
}
```

## Einsatz von Variablen beim Coden

```java

package com.bit.java_project //Strukturverzeichnis des Packages

pubblic class Variablen{ //Class 
    pubblic static void main(string[]args){ // Main-Funktion
        int value = 10;
        int x = value;
        System.out.println("Value of my Variable: " + x);
    }
}
```

[Übung mit Variablen](https://github.com/Pierre890/java_experience/blob/main/src/main/java/java_experience/datatyp.java)

## Operatoren 

In Java sind Operatoren Symbole, die bestimmte mathematische Operationen durchführen. 
Java hat eine Vielzahl von Operatoren, darunter:

- **Arithmetische Operatoren:** führen grundlegende arithmetische Operationen wie Addition, Subtraktion, Multiplikation, Division und Modul durch.

- **Vergleichsoperatoren:** vergleichen zwei Werte und geben ein boolesches Ergebnis (true oder false) zurück.

- **Logische Operatoren:** führen logische Operationen wie "AND" (&&), "OR" (||) und "NOT" (!=) durch.

- **Zuweisungsoperatoren:** weisen einem Variablen einen Wert zu.

- **Bedingungsoperatoren:** werden verwendet, um bedingte Anweisungen wie "if-else" und "switch-case" zu erstellen.

- **Ternärer Operator:** kurzform für das Schreiben einer bedingten Anweisung, die einen Wert zurückgibt.

Hier ist ein Beispiel dafür, wie einige dieser Operatoren in Java verwendet werden können:

```java
int x = 10;
int y = 5;

int sum = x + y;       // 15
int difference = x - y; // 5
int product = x * y;    // 50
int quotient = x / y;   // 2
int remainder = x % y;  // 0

boolean isEqual = (x == y);  // false
boolean isGreater = (x > y); // true

x += y;  // x is now 15
x *= y;  // x is now 75

int min = (x < y) ? x : y; // min is 5
```

[Übung mit Operatoren](https://github.com/Pierre890/java_experience/blob/main/src/main/java/java_experience/operators.java)

## If/Else - Statement

Ein if-else-Statement in Java ist eine bedingte Anweisung, die es ermöglicht, bestimmte Codeblöcke auszuführen, je nachdem, ob eine bestimmte Bedingung wahr oder falsch ist. Wird eine bestimmte Bedingung erfüllt gehört sie zum If-Teil, sonst zum Else-Teil (nicht erfüllt).

Die Syntax für ein if-else-Statement lautet wie folgt:

```java
if (bedingung) {
   // Code ausführen, wenn die Bedingung wahr ist
} else {
   // Code ausführen, wenn die Bedingung falsch ist
}
```
Hier ist ein Beispiel für ein If/Else-Statement in Java:

```java
int x = 10;
int y = 5;

if (x > y) {
  System.out.println("x is greater than y");
} else {
  System.out.println("x is not greater than y");
}
```
In diesem Beispiel wird die Ausgabe "*x is greater than y*" sein, da die Bedingung x > y wahr ist. Wenn die Bedingung nicht wahr gewesen wäre, würde die Else-Anweisung ausgeführt, sodass die Ausgabe "*x is not greater than y*" wäre.

Es ist auch möglich, mehrere bedingte Anweisungen mithilfe von "else if" zu verkettem, wie in folgendem Beispiel gezeigt:

```java
int x = 10;
int y = 5;

if (x > y) {
  System.out.println("x is greater than y");
} else if (x < y) {
  System.out.println("x is less than y");
} else {
  System.out.println("x is equal to y");
}
```

In diesem Beispiel wird die Ausgabe "*x is greater than y*" sein, da die Bedingung x > y wahr ist. Wenn die Bedingung x > y nicht wahr ist, wird die nächste Bedingung x < y überprüft. Wenn auch diese Bedingung nicht wahr ist, wird die Else-Anweisung ausgeführt und die Ausgabe wäre "*x is equal to y*".

## Switch Statement

Wenn die if/else statements zu kompliziert und zu lang zu programmieren werden, können sie vom "Switch" ersetzt werden. 

Hier ist ein Beispiel für ein Switch-Statement:

```java
int x = 2;

switch (x) { // bediengung
  case 1:
    System.out.println("x is 1"); 
    break;
  case 2:
    System.out.println("x is 2");
    break;
  case 3:
    System.out.println("x is 3");
    break;
  default:
    System.out.println("x is not 1, 2, or 3");
    break;
}
```
In diesem Beispiel wird die Ausgabe "*x is 2*" sein, da der Wert von x mit dem Case-Label 2 übereinstimmt. Wenn keines der case-Labels mit dem Wert von x übereinstimmt, wird der default-Block ausgeführt.

Es ist wichtig zu beachten, dass der Ausdruck, der im Switch- Statement verwendet wird, bestimmte Typen haben muss. Der Ausdruck kann eine ganze Zahl, ein Zeichen oder ein String sein.

## Scanner (User Imput)

Die Scanner-Klasse gehört zur Bibliothek "java.util" der "Java Standard Library" und ermöglicht, Daten von der Standardeingabe (normalerweise die Tastatur) einzulesen.
Um den Scanner verwenden zu können, muss er ins Projekt importiert werden. Beispiel:

```java
import java.util.Scanner; //die Scanner-Klasse wird importiert

public class Main {

  private static Scanner input = new Scanner(System.in); //globale Einstellung

  public static void main(String[] args) {

    System.out.print("Enter your name: ");
    String name = input.nextLine(); //liest einen String ein.

    System.out.print("Enter your age: ");
    int age = input.nextInt(); //liest einen Integer ein.

    System.out.println("Your name is " + name + " and you are " + age + " years old.");

    input.close(); //Der Scanner wird geschlossen um Resource-Leak (Memory Leak) von Java zu meiden. 
  }
}
```

In diesem Beispiel wird der Benutzer aufgefordert, seinen Namen und sein Alter einzugeben. Die Eingabe wird dann von der nextLine()-Methode für den Namen und der nextInt()-Methode für das Alter eingelesen. Die eingelesenen Werte werden dann in den Variablen name und age gespeichert und zusammen mit einer Ausgabe auf der Konsole ausgegeben.

Der Scanner kann auch verwendet werden, um andere primitive Datentypen wie double, float, long, und short sowie boolean-Werte und Zeichen einzulesen. Um diese Inputs einlesen zu können, gilt folgende Tabelle:

![](input.drawio.png)

[Aufgabe 1: Input/Switch](https://github.com/Pierre890/java_experience/blob/main/src/main/java/java_experience/switch_input.java)

[Aufgabe 2: Input/Switch](https://github.com/Pierre890/java_experience/blob/main/src/main/java/java_experience/switch_input_char.java)

## Arrays

Arrays sind ein spezieller Typ von Objekten, die mehrere Elemente (Variablen) des gleichen Typs enthalten können. Beispiel:

```java
String[] fruits_array = {"Apple", "Orange", "Banana", "Lemon"};
// Veriable (name)    = {0,1,2,3}
                    // index (position) der Elementen in der Array
```
Diese Array hat Länge (length) 4. Um ein Element aus der Array auszugeben:

`Sistem.out.println("first array element: " + fruits_array[0]);`
`Sistem.out.println("third array element: " + fruits_array[2]);`

Um die Länge der Array auszugeben:

`Sistem.out.println(fruits_array.length);`

## Loops (Schleifen)

Schleifenstrukturen werden verwendet, um bestimmte Code-Abschnitte mehrfach auszuführen. Die drei am häufigsten verwendeten Schleifen sind die "**for-Schleife**", die "**while-Schleife**" und die "**do-while-Schleife**".

### For-Loop

Die "for-Schleife" wird verwendet, wenn die Anzahl der Durchläufe im Voraus bekannt ist. Sie hat die folgende Syntax:

```java
for (Initialisierung; Bedingung; Schritte) {
    // Code der wiederholt ausgeführt werden soll
}
```
Die initialisierung wird einmal vor dem Start der Schleife ausgeführt, die Bedingung wird vor jedem Durchlauf geprüft und falls sie "true" ergibt, wird der Code in der Schleife ausgeführt, sonst wird die Schleife beendet. Schritte werden nach jedem Durchlauf ausgeführt. Für das vorherige Array-Beispiel können wir eine Schleife einbauen, die alle Elemente der Array ausgibt:

```java
String[] fruits_array = {"Apple", "Orange", "Banana", "Lemon"};
  for (int i = 0; i < fruits_array.length; i++){
    System.out.println("fruits: " + fruits_array[i];)
  }
```
Im Beispiel ist "i = 0" die Initialisierung. Hier startet die Schleife und gibt im Terminal das erste Array-Element aus, solange die Bediengung erfüllt wird. Da die Array Länge 4 hat, braucht man 4 Iterationen (bis zur Position 3), bis alle Elemente ausgegeben sind.

[For-Loop Übung 1](https://github.com/Pierre890/java_experience/blob/main/src/main/java/java_experience/arrays.java)
[For-Loop Übung 2](https://github.com/Pierre890/java_experience/blob/main/src/main/java/java_experience/fizzbazz.java)

### While-Loop

Die "while-Schleife" wird verwendet, wenn die Anzahl der Durchläufe nicht im Voraus bekannt ist. Sie hat die folgende Syntax:

```java
while (Bedingung) {
    // Code der wiederholt ausgeführt werden soll
}
```

Die Bedingung wird vor jedem Durchlauf der Schleife geprüft und falls sie true ist, wird der Code in der Schleife ausgeführt, sonst beendet die Schleife.

[While-Loop Übung 1](https://github.com/Pierre890/java_experience/blob/main/src/main/java/java_experience/while_loop.java)
[While-Loop Übung 2](https://github.com/Pierre890/java_experience/blob/main/src/main/java/java_experience/two_imputs.java)

### Do-While-Loop

Die "do-while-Schleife" ist ähnlich wie die while-Schleife, aber der Code in der Schleife wird mindestens einmal ausgeführt, bevor die Bedingung geprüft wird. Sie hat die folgende Syntax:

```java
do {
    // Code der wiederholt ausgeführt werden soll
} while (Bedingung);
```

Für ihre Komplexität wird diese Schleife sehr seltern in die Praxis eingesetzt.
