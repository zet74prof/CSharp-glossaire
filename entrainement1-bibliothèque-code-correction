#### Exemple de Code

```csharp
using System;
using System.Collections.Generic;

class Program
{
    static int totalBooks = 50;
    static int borrowedBooks = 0;
    static string[] userNames = new string[50];
    static int userCount = 0;
    static List<DateTime> borrowDates = new List<DateTime>();
    static int borrowDuration = 14; // Durée par défaut de 14 jours

    static void Main()
    {
        string continueBorrowing = "oui";
        while (continueBorrowing.ToLower() == "oui")
        {
            Console.Write("Entrez votre nom : ");
            string userName = Console.ReadLine();

            Console.Write("Entrez le nombre de livres que vous souhaitez emprunter : ");
            int booksToBorrow = int.Parse(Console.ReadLine());

            if (booksToBorrow <= (totalBooks - borrowedBooks))
            {
                AjouterEmprunt(userName, booksToBorrow);
            }
            else
            {
                Console.WriteLine("Désolé, le nombre de livres demandés n'est pas disponible.");
            }

            Console.Write("Souhaitez-vous faire un nouvel emprunt ? (oui/non) : ");
            continueBorrowing = Console.ReadLine();
        }

        string continueDisplay = "oui";
        do
        {
            AfficherEmprunts();
            Console.Write("Souhaitez-vous continuer à afficher les emprunts ? (oui/non) : ");
            continueDisplay = Console.ReadLine();
        } while (continueDisplay.ToLower() == "oui");

        AfficherDisponibilites();

        Console.WriteLine("Dates d'emprunt :");
        foreach (var date in borrowDates)
        {
            Console.WriteLine(date);
        }
    }

    static void AfficherDisponibilites()
    {
        Console.WriteLine("Disponibilités des livres pour les prochains 7 jours :");
        for (int i = 0; i < 7; i++)
        {
            Console.WriteLine($"Jour {i + 1} : {totalBooks - borrowedBooks} livres disponibles.");
        }
    }

    static void AjouterEmprunt(string nom, int nombreLivres)
    {
        borrowedBooks += nombreLivres;
        DateTime borrowDate = DateTime.Now;
        userNames[userCount] = nom;
        userCount++;
        borrowDates.Add(borrowDate);
        Console.WriteLine($"Emprunt confirmé pour {nom} le {borrowDate}. Durée de l'emprunt : {borrowDuration} jours.");
    }

    static void AfficherEmprunts()
    {
        Console.WriteLine("Emprunts en cours :");
        for (int i = 0; i < userCount; i++)
        {
            Console.WriteLine($"Utilisateur : {userNames[i]}, Date d'emprunt : {borrowDates[i]}, Livres empruntés : {borrowedBooks}, Durée de l'emprunt : {borrowDuration} jours.");
        }
    }
}
```
