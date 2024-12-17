### **Évaluation d'entraînement : Gestion des Rendez-Vous d'un Hôpital Public**

---

#### **Exercice 1 : Déclaration de variables et types de données** (5 points)  
1. Déclarez les variables nécessaires pour stocker :  
   - Le nombre total de médecins disponibles.  
   - Le nombre total de salles de consultation disponibles.  
   - Le nom du patient.  
   - Le type de consultation souhaitée (généraliste ou spécialiste) (où `Vrai` = spécialiste et `Faux` = généraliste).  
   - La durée estimée de la consultation en minutes.  

2. Assignez des valeurs initiales aux variables en supposant :  
   - 5 médecins généralistes disponibles.  
   - 3 médecins spécialistes disponibles.  
   - 8 salles de consultation disponibles.  
   - Le type de consultation par défaut est généraliste (ie `Faux`).  

---

#### **Exercice 2 : Conditions et prise de décision** (10 points)  
Écrivez un programme qui :  
1. Demande à l'utilisateur le type de consultation souhaitée : 1 pour généraliste / 2 pour spécialiste.  
2. Vérifie si un médecin correspondant est disponible :  
   - Si oui, passe le type de consultation à `true` pour spécialiste ou `false` pour généraliste.  
   - Réserve un médecin et une salle si les ressources sont disponibles, puis affiche un message de confirmation.  
   - Si non, affiche un message d’erreur indiquant qu’aucune ressource n’est disponible.  

Exemple :  
```
Quel type de consultation souhaitez-vous ? Saisissez 1 pour généraliste ou 2 pour spécialiste : 2
Une consultation chez un spécialiste est disponible. Votre rendez-vous est confirmé.
```

---

#### **Exercice 3 : Boucles et validation des entrées** (15 points)  
1. Modifiez le programme précédent pour que l'utilisateur puisse réessayer en cas de demande incorrecte.  
   - Utilisez une boucle `do...while` pour répéter la demande tant que le type de consultation ou le nombre de médecins disponibles est incorrect.  
   - Validez l'entrée pour s'assurer que l'utilisateur saisit bien un entier correspondant au type de consultation.  

Exemple :  
```
Quel type de consultation souhaitez-vous ? abc
Veuillez saisir un nombre valide.
Quel type de consultation souhaitez-vous ? 3
Option non valide. Veuillez choisir 1 pour généraliste ou 2 pour spécialiste.
```

---

#### **Exercice 4 : Utilisation des tableaux et des listes** (20 points)  
1. Déclarez un tableau contenant les noms de 5 patients fictifs ayant déjà pris un rendez-vous.  
2. Affichez les noms des patients à l'aide d'une boucle `foreach`.  
3. Ajoutez une fonctionnalité pour ajouter un nouveau patient à une liste dynamique après une réservation valide.  
4. Affichez la liste mise à jour après chaque ajout.

---

#### **Exercice 5 : Création de fonctions** (20 points)  
1. Implémentez une fonction `CalculerTempsTotalOccupé` qui prend en paramètre :    
   - Le nombre de rendez-vous réservés.  
   - La durée moyenne d'une consultation.  
   - Et retourne le temps total occupé pour tous les rendez-vous.  

2. Appelez cette fonction après chaque réservation et affichez le temps total estimé pour toutes les consultations.

---

#### **Exercice 6 : Mise en application complète** (30 points)  
Créez un programme complet en combinant les exercices précédents :  
1. Demandez à l'utilisateur de saisir :  
   - Son nom.  
   - Le type de consultation souhaitée (généraliste/spécialiste).  
   - La durée estimée de la consultation.  

2. Validez les données saisies avec des boucles et conditions appropriées.  
3. Appelez la fonction `CalculerTempsTotalOccupé` pour afficher la charge de travail estimée de l'hôpital.  
4. Ajoutez le nom du patient à une liste dynamique et réduisez le nombre de médecins et de salles disponibles.  
5. Affichez un résumé à la fin :  
   - Nom du patient.  
   - Type de consultation.  
   - Durée estimée.  
   - Médecins restants.  
   - Salles restantes.

Exemple de sortie :  
```
Nom du patient : Claire  
Type de consultation : Spécialiste  
Durée estimée : 30 minutes  
Médecins restants : 2  
Salles restantes : 7  
Temps total occupé pour toutes les consultations : 150 minutes.
```

---

### **Barème total : 100 points**  
- Variables : 5 points  
- Conditions : 10 points  
- Boucles : 15 points  
- Tableaux et listes : 20 points  
- Fonctions : 20 points  
- Mise en application complète : 30 points  
