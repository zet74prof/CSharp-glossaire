### **Corrigé : Application de gestion des rendez-vous d’un hôpital public**

---

#### **Exercice 1 : Déclaration de variables et types de données**

```csharp
// Déclaration des variables
int medecinsGeneralistes = 5;
int medecinsSpecialistes = 3;
int sallesDisponibles = 8;
string nomPatient = "";
bool typeConsultation = false; // false = généraliste, true = spécialiste
int dureeConsultation = 0;

// Affichage des valeurs par défaut
Console.WriteLine("Variables initialisées pour l'hôpital :");
Console.WriteLine($"Médecins généralistes : {medecinsGeneralistes}");
Console.WriteLine($"Médecins spécialistes : {medecinsSpecialistes}");
Console.WriteLine($"Salles disponibles : {sallesDisponibles}");
```

---

#### **Exercice 2 : Conditions et prise de décision**

```csharp
Console.WriteLine("Quel type de consultation souhaitez-vous ? Saisissez 1 pour généraliste ou 2 pour spécialiste.");
int choix = int.Parse(Console.ReadLine());

if (choix == 1)
{
    typeConsultation = false; // Consultation généraliste
    if (medecinsGeneralistes > 0 && sallesDisponibles > 0)
    {
        Console.WriteLine("Une consultation chez un généraliste est disponible. Votre rendez-vous est confirmé.");
        medecinsGeneralistes--;
        sallesDisponibles--;
    }
    else
    {
        Console.WriteLine("Désolé, aucune ressource disponible pour une consultation généraliste.");
    }
}
else if (choix == 2)
{
    typeConsultation = true; // Consultation spécialiste
    if (medecinsSpecialistes > 0 && sallesDisponibles > 0)
    {
        Console.WriteLine("Une consultation chez un spécialiste est disponible. Votre rendez-vous est confirmé.");
        medecinsSpecialistes--;
        sallesDisponibles--;
    }
    else
    {
        Console.WriteLine("Désolé, aucune ressource disponible pour une consultation spécialiste.");
    }
}
else
{
    Console.WriteLine("Option invalide. Veuillez choisir 1 pour généraliste ou 2 pour spécialiste.");
}
```

---

#### **Exercice 3 : Boucles et validation des entrées**

```csharp
int choix;
bool manqueRessources = false;

do
{
    Console.WriteLine("Quel type de consultation souhaitez-vous ? Saisissez 1 pour généraliste ou 2 pour spécialiste.");
    while (!int.TryParse(Console.ReadLine(), out choix) || (choix != 1 && choix != 2))
    {
        Console.WriteLine("Option non valide. Veuillez saisir 1 ou 2.");
    }

    if (choix == 1 && medecinsGeneralistes > 0 && sallesDisponibles > 0)
    {
        typeConsultation = false; // Généraliste
        medecinsGeneralistes--;
        sallesDisponibles--;
        Console.WriteLine("Votre rendez-vous chez un généraliste est confirmé.");
    }
    else if (choix == 2 && medecinsSpecialistes > 0 && sallesDisponibles > 0)
    {
        typeConsultation = true; // Spécialiste
        medecinsSpecialistes--;
        sallesDisponibles--;
        Console.WriteLine("Votre rendez-vous chez un spécialiste est confirmé.");
    }
    else
    {
        Console.WriteLine("Désolé, aucune ressource disponible pour ce type de consultation.");
        manqueRessources = true;
    }
} while (manqueRessources);
```

---

#### **Exercice 4 : Utilisation des tableaux et des listes**

```csharp
// Déclaration du tableau des patients fictifs
string[] patientsFictifs = { "Alice", "Bob", "Charlie", "Diana", "Eve" };
Console.WriteLine("Patients ayant déjà pris rendez-vous :");
foreach (string patient in patientsFictifs)
{
    Console.WriteLine($"- {patient}");
}

// Liste dynamique pour les nouveaux patients
List<string> listePatients = new List<string>(patientsFictifs);

// Ajout d’un nouveau patient après réservation
Console.WriteLine("\nEntrez le nom du nouveau patient :");
nomPatient = Console.ReadLine();
listePatients.Add(nomPatient);

Console.WriteLine("\nListe mise à jour des patients ayant pris rendez-vous :");
foreach (string patient in listePatients)
{
    Console.WriteLine($"- {patient}");
}
```

---

#### **Exercice 5 : Création de fonctions**

```csharp
static int CalculerTempsTotalOccupé(int nombreRendezVous, int dureeMoyenne)
{
    return nombreRendezVous * dureeMoyenne;
}

// Exemple d’utilisation
int nombreRendezVous = 5; // Exemple : 5 rendez-vous
int dureeMoyenne = typeConsultation ? 45 : 30; // 45 min pour spécialiste, 30 min pour généraliste
int tempsTotal = CalculerTempsTotalOccupé(typeConsultation, nombreRendezVous, dureeMoyenne);
Console.WriteLine($"Temps total occupé pour toutes les consultations : {tempsTotal} minutes.");
```

---

#### **Exercice 6 : Mise en application complète**

```csharp
// Programme complet combinant les éléments précédents
Console.WriteLine("Entrez votre nom :");
nomPatient = Console.ReadLine();

do
{
    Console.WriteLine("Quel type de consultation souhaitez-vous ? Saisissez 1 pour généraliste ou 2 pour spécialiste.");
    while (!int.TryParse(Console.ReadLine(), out choix) || (choix != 1 && choix != 2))
    {
        Console.WriteLine("Option non valide. Veuillez saisir 1 ou 2.");
    }

    if (choix == 1 && medecinsGeneralistes > 0 && sallesDisponibles > 0)
    {
        typeConsultation = false;
        medecinsGeneralistes--;
        sallesDisponibles--;
        break;
    }
    else if (choix == 2 && medecinsSpecialistes > 0 && sallesDisponibles > 0)
    {
        typeConsultation = true;
        medecinsSpecialistes--;
        sallesDisponibles--;
        break;
    }
    else
    {
        Console.WriteLine("Désolé, aucune ressource disponible pour ce type de consultation.");
    }
} while (true);

Console.WriteLine("Durée estimée de la consultation (en minutes) :");
while (!int.TryParse(Console.ReadLine(), out dureeConsultation) || dureeConsultation <= 0)
{
    Console.WriteLine("Veuillez entrer une durée valide.");
}

// Calcul du temps total
tempsTotal = CalculerTempsTotalOccupé(typeConsultation, 1, dureeConsultation);
listePatients.Add(nomPatient);

Console.WriteLine("\nRésumé de la réservation :");
Console.WriteLine($"Nom du patient : {nomPatient}");
Console.WriteLine($"Type de consultation : {(typeConsultation ? "Spécialiste" : "Généraliste")}");
Console.WriteLine($"Durée estimée : {dureeConsultation} minutes");
Console.WriteLine($"Médecins restants : {(typeConsultation ? medecinsSpecialistes : medecinsGeneralistes)}");
Console.WriteLine($"Salles restantes : {sallesDisponibles}");
Console.WriteLine($"Temps total occupé : {tempsTotal} minutes.");
```
