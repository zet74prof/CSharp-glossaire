### **Glossaire des Éléments de base du langage C#**

#### **1. Variables et Types de Données**
- **Définition :** Une variable est une unité de stockage qui permet de conserver des données en mémoire.
- **Types de données courants :**
  - `int` : Pour les nombres entiers (exemple : `int age = 25;`).
  - `double` : Pour les nombres à virgule flottante (exemple : `double prix = 19.99;`).
  - `string` : Pour les chaînes de caractères (exemple : `string nom = "Alice";`).
  - `bool` : Pour les valeurs booléennes (vrai ou faux) (exemple : `bool estActif = true;`).
  - `decimal` : Pour les valeurs numériques précises, souvent utilisées pour des prix (exemple : `decimal montant = 15.50m;`).

---

#### **2. Conditions (if, else if, else)**
- **Définition :** Les conditions permettent d'exécuter des blocs de code en fonction d'une condition donnée.
- **Exemple :**
  ```csharp
  int nombre = 10;
  if (nombre > 5)
  {
      Console.WriteLine("Le nombre est supérieur à 5.");
  }
  else if (nombre == 5)
  {
      Console.WriteLine("Le nombre est égal à 5.");
  }
  else
  {
      Console.WriteLine("Le nombre est inférieur à 5.");
  }
  ```

---

#### **3. Boucles**
- **Définition :** Les boucles permettent de répéter un bloc de code tant qu'une condition est vraie.
- **Types courants :**
  - **`for`** : Pour un nombre de répétitions connu.
    ```csharp
    for (int i = 0; i < 5; i++)
    {
        Console.WriteLine($"Itération {i}");
    }
    ```
  - **`while`** : Tant qu'une condition est vraie.
    ```csharp
    int compteur = 0;
    while (compteur < 5)
    {
        Console.WriteLine($"Compteur : {compteur}");
        compteur++;
    }
    ```
  - **`do...while`** : Exécute au moins une fois avant de vérifier la condition.
    ```csharp
    int compteur = 0;
    do
    {
        Console.WriteLine($"Compteur : {compteur}");
        compteur++;
    } while (compteur < 5);
    ```
  - **`foreach`** : Pour parcourir les éléments d'une collection.
    ```csharp
    string[] noms = { "Alice", "Bob", "Charlie" };
    foreach (string nom in noms)
    {
        Console.WriteLine(nom);
    }
    ```

---

#### **4. Tableaux et Listes**
- **Tableau (Array)** :
  - **Définition :** Une collection de taille fixe pour stocker des éléments de même type.
  - **Exemple :**
    ```csharp
    int[] nombres = { 1, 2, 3, 4, 5 };
    Console.WriteLine(nombres[0]); // Affiche 1
    ```
- **Liste (List)** :
  - **Définition :** Une collection dynamique pouvant changer de taille.
  - **Exemple :**
    ```csharp
    List<string> noms = new List<string> { "Alice", "Bob" };
    noms.Add("Charlie");
    Console.WriteLine(noms[2]); // Affiche Charlie
    ```

---

#### **5. Fonctions (Méthodes)**
- **Définition :** Les fonctions encapsulent des blocs de code pour les réutiliser et les rendre plus modulaires.
- **Syntaxe :**
  ```csharp
  // Déclaration d'une fonction
  static int Addition(int a, int b)
  {
      return a + b;
  }

  // Appel de la fonction
  int resultat = Addition(5, 3);
  Console.WriteLine(resultat); // Affiche 8
  ```

---

#### **6. Entrées et Sorties (I/O)**
- **Entrée utilisateur :**
  ```csharp
  Console.WriteLine("Entrez votre nom :");
  string nom = Console.ReadLine();
  Console.WriteLine($"Bonjour, {nom} !");
  ```
- **Sortie utilisateur :**
  ```csharp
  Console.WriteLine("Ceci est un message.");
  ```

---

#### **7. Gestion de la Date et de l’Heure**
- **Obtenir la date et l'heure actuelles :**
  ```csharp
  DateTime maintenant = DateTime.Now;
  Console.WriteLine($"Date actuelle : {maintenant}");
  ```
- **Ajouter des jours à une date :**
  ```csharp
  DateTime dateRetour = DateTime.Now.AddDays(7);
  Console.WriteLine($"Date de retour prévue : {dateRetour}");
  ```

---
