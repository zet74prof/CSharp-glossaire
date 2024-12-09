### **Code de Correction : Application de gestion d'une bibliothèque**
```csharp
using System;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        // Variables
        int totalLivres = 100;
        List<string> livresEmpruntes = new List<string>();
        string[] livresPopulaires = { "Le Petit Prince", "1984", "L'Alchimiste", "Harry Potter", "Les Misérables" };

        Console.WriteLine("Bienvenue dans l'application de gestion de la bibliothèque !");
        Console.WriteLine("\nVoici les livres populaires disponibles :");

        // Affichage des livres populaires
        foreach (var livre in livresPopulaires)
        {
            Console.WriteLine($"- {livre}");
        }

        // Début de l'emprunt
        Console.WriteLine("\nEntrez votre nom :");
        string nomEmprunteur = Console.ReadLine();

        string titreLivre;
        do
        {
            Console.WriteLine("\nQuel livre souhaitez-vous emprunter ?");
            titreLivre = Console.ReadLine();

            if (string.IsNullOrWhiteSpace(titreLivre))
            {
                Console.WriteLine("Le titre ne peut pas être vide. Veuillez entrer un titre valide.");
            }
        } while (string.IsNullOrWhiteSpace(titreLivre));

        if (totalLivres <= 0)
        {
            Console.WriteLine($"Désolé, il n'y a plus de livres disponibles pour \"{titreLivre}\".");
        }
        else
        {
            totalLivres--;
            livresEmpruntes.Add(titreLivre);

            Console.WriteLine("\nCombien de jours souhaitez-vous emprunter ce livre ?");
            int dureeEmprunt;
            while (!int.TryParse(Console.ReadLine(), out dureeEmprunt) || dureeEmprunt <= 0)
            {
                Console.WriteLine("Veuillez entrer une durée valide (en jours).");
            }

            // Calcul de la date de retour
            DateTime dateRetour = CalculerDateRetour(dureeEmprunt);

            // Résumé de l'emprunt
            Console.WriteLine("\nRésumé de votre emprunt :");
            Console.WriteLine($"Nom de l'emprunteur : {nomEmprunteur}");
            Console.WriteLine($"Livre emprunté : {titreLivre}");
            Console.WriteLine($"Durée de l'emprunt : {dureeEmprunt} jours");
            Console.WriteLine($"Date de retour prévue : {dateRetour:yyyy-MM-dd}");
            Console.WriteLine($"Livres restants dans la bibliothèque : {totalLivres}");

            Console.WriteLine("\nListe mise à jour des livres empruntés :");
            foreach (var livre in livresEmpruntes)
            {
                Console.WriteLine($"- {livre}");
            }

            Console.WriteLine("\nMerci pour votre emprunt !");
        }
    }

    // Fonction pour calculer la date de retour
    static DateTime CalculerDateRetour(int dureeEnJours)
    {
        return DateTime.Now.AddDays(dureeEnJours);
    }
}
```

---

### **Explications des points clés :**

1. **Variables et initialisation**  
   - `totalLivres` : Stocke le nombre total de livres disponibles.
   - `livresPopulaires` : Tableau contenant les titres des livres populaires.
   - `livresEmpruntes` : Liste dynamique pour suivre les livres empruntés.

2. **Validation des données avec boucles et conditions**  
   - Vérifie que le titre saisi n'est pas vide.  
   - Vérifie que la durée d'emprunt est un entier positif.

3. **Tableaux et listes**  
   - Le tableau `livresPopulaires` est utilisé pour afficher les titres populaires.  
   - La liste `livresEmpruntes` est mise à jour après chaque emprunt.

4. **Fonctions**  
   - La fonction `CalculerDateRetour` retourne la date de retour prévue en ajoutant la durée d'emprunt à la date actuelle.

5. **Interaction utilisateur**  
   - Le programme guide l'utilisateur à travers les étapes de l'emprunt, valide les entrées, et affiche un résumé complet.

---

### **Exemple de Sortie :**
```
Bienvenue dans l'application de gestion de la bibliothèque !

Voici les livres populaires disponibles :
- Le Petit Prince
- 1984
- L'Alchimiste
- Harry Potter
- Les Misérables

Entrez votre nom :
Marie

Quel livre souhaitez-vous emprunter ?
Le Petit Prince

Combien de jours souhaitez-vous emprunter ce livre ?
7

Résumé de votre emprunt :
Nom de l'emprunteur : Marie
Livre emprunté : Le Petit Prince
Durée de l'emprunt : 7 jours
Date de retour prévue : 2024-12-16
Livres restants dans la bibliothèque : 99

Liste mise à jour des livres empruntés :
- Le Petit Prince

Merci pour votre emprunt !
```
