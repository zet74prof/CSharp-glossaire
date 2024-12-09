### Glossaire des Éléments de Code en C#

Ce glossaire couvre les éléments de base de la programmation en C# nécessaires pour les évaluations proposées. Chaque élément est accompagné d'un exemple de code neutre pour illustrer son utilisation.

#### 1. Variables et Types de Données de Base

- **Variable** : Un conteneur pour stocker des données.
  ```csharp
  int number = 42; // Variable de type entier
  string name = "Alice"; // Variable de type chaîne de caractères
  double price = 19.99; // Variable de type double
  DateTime currentDate = DateTime.Now; // Variable de type DateTime
  ```

- **Types de Données de Base** :
  - `int` : Entier
  - `string` : Chaîne de caractères
  - `double` : Nombre à virgule flottante
  - `DateTime` : Date et heure

#### 2. Tableaux

- **Tableau** : Une collection d'éléments du même type.
  ```csharp
  int[] numbers = new int[5]; // Tableau d'entiers
  numbers[0] = 10; // Ajout d'un élément au tableau
  ```

#### 3. Listes

- **Liste** : Une collection dynamique d'éléments du même type.
  ```csharp
  List<string> names = new List<string>(); // Liste de chaînes de caractères
  names.Add("Bob"); // Ajout d'un élément à la liste
  ```

#### 4. Instructions Conditionnelles

- **if, else if, else** : Utilisées pour exécuter du code en fonction de conditions.
  ```csharp
  int age = 18;
  if (age < 18)
  {
      Console.WriteLine("Vous êtes mineur.");
  }
  else if (age == 18)
  {
      Console.WriteLine("Vous avez 18 ans.");
  }
  else
  {
      Console.WriteLine("Vous êtes majeur.");
  }
  ```

#### 5. Boucles Itératives

- **while** : Exécute un bloc de code tant qu'une condition est vraie.
  ```csharp
  int count = 0;
  while (count < 5)
  {
      Console.WriteLine("Count is: " + count);
      count++;
  }
  ```

- **do...while** : Exécute un bloc de code au moins une fois, puis continue tant qu'une condition est vraie.
  ```csharp
  int count = 0;
  do
  {
      Console.WriteLine("Count is: " + count);
      count++;
  } while (count < 5);
  ```

- **for** : Exécute un bloc de code un nombre spécifié de fois.
  ```csharp
  for (int i = 0; i < 5; i++)
  {
      Console.WriteLine("Iteration: " + i);
  }
  ```

- **foreach** : Parcourt les éléments d'une collection.
  ```csharp
  List<string> fruits = new List<string> { "Apple", "Banana", "Cherry" };
  foreach (var fruit in fruits)
  {
      Console.WriteLine("Fruit: " + fruit);
  }
  ```

#### 6. Fonctions

- **Fonction** : Un bloc de code réutilisable qui effectue une tâche spécifique.
  ```csharp
  static void Greet(string name)
  {
      Console.WriteLine("Hello, " + name + "!");
  }

  static int Add(int a, int b)
  {
      return a + b;
  }

  static void Main()
  {
      Greet("Alice"); // Appel de la fonction Greet
      int sum = Add(3, 4); // Appel de la fonction Add
      Console.WriteLine("Sum: " + sum);
  }
  ```

#### Exemple Complet

Voici un exemple complet utilisant tous les éléments de code nécessaires dans un contexte neutre :

```csharp
using System;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        // Déclaration de variables
        int number = 42;
        string name = "Alice";
        double price = 19.99;
        DateTime currentDate = DateTime.Now;

        // Utilisation de tableaux
        int[] numbers = new int[5];
        numbers[0] = 10;

        // Utilisation de listes
        List<string> names = new List<string>();
        names.Add("Bob");

        // Instructions conditionnelles
        int age = 18;
        if (age < 18)
        {
            Console.WriteLine("Vous êtes mineur.");
        }
        else if (age == 18)
        {
            Console.WriteLine("Vous avez 18 ans.");
        }
        else
        {
            Console.WriteLine("Vous êtes majeur.");
        }

        // Boucle while
        int count = 0;
        while (count < 5)
        {
            Console.WriteLine("Count is: " + count);
            count++;
        }

        // Boucle do...while
        count = 0;
        do
        {
            Console.WriteLine("Count is: " + count);
            count++;
        } while (count < 5);

        // Boucle for
        for (int i = 0; i < 5; i++)
        {
            Console.WriteLine("Iteration: " + i);
        }

        // Boucle foreach
        List<string> fruits = new List<string> { "Apple", "Banana", "Cherry" };
        foreach (var fruit in fruits)
        {
            Console.WriteLine("Fruit: " + fruit);
        }

        // Utilisation de fonctions
        Greet("Alice");
        int sum = Add(3, 4);
        Console.WriteLine("Sum: " + sum);
    }

    static void Greet(string name)
    {
        Console.WriteLine("Hello, " + name + "!");
    }

    static int Add(int a, int b)
    {
        return a + b;
    }
}
```
