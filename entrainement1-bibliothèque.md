### **Entraînement : Application de gestion d'une bibliothèque**  
#### **Contexte :**  
Une bibliothèque souhaite numériser son système de gestion pour gérer les emprunts de livres. Vous devez écrire un programme simple en C# qui facilite cette gestion.

---

### **Exercice 1 : Déclaration de variables et types de données** (5 points)  
1. Déclarez les variables nécessaires pour stocker :  
   - Le nombre total de livres disponibles.  
   - Le titre du livre emprunté.  
   - Le nom de l'emprunteur.  
   - La durée de l'emprunt en jours.  

2. Assignez des valeurs initiales aux variables en supposant :  
   - 100 livres disponibles.  
   - Pas encore de titre emprunté.  

---

### **Exercice 2 : Conditions et prise de décision** (10 points)  
Écrivez un programme qui :  
1. Demande à l'utilisateur le titre du livre qu'il souhaite emprunter.  
2. Vérifie si le livre est disponible (en supposant qu'il y a 100 copies disponibles pour tous les livres).  
3. Affiche :  
   - Un message de confirmation si le livre est disponible.  
   - Un message d’erreur si aucun exemplaire n’est disponible (livres restants = 0).  

Exemple :  
```
Quel livre souhaitez-vous emprunter ? "Le Petit Prince"
Le livre "Le Petit Prince" est disponible. Votre emprunt est confirmé.
```

---

### **Exercice 3 : Boucles et validation des entrées** (15 points)  
1. Modifiez le programme précédent pour permettre à l'utilisateur de réessayer si le titre saisi est vide.  
   - Utilisez une boucle `do...while` pour répéter la demande tant que l'utilisateur n'entre pas un titre valide (non vide).
   - Vous pouvez utiliser la méthode `string.IsNullOrWhiteSpace(uneChaine)` qui retourne vrai si la variable passée en paramètre ne contient aucun caractère ou que des espaces, et faux sinon.

---

### **Exercice 4 : Utilisation des tableaux et des listes** (20 points)  
1. Déclarez un tableau contenant les noms de 5 livres populaires disponibles dans la bibliothèque.  
2. Affichez ces titres à l'aide d'une boucle `foreach`.  
3. Ajoutez une fonctionnalité permettant de suivre les titres empruntés en déclarant une liste dynamique et en ajoutant le titre d'un livre saisi par l'utilisateur à cette liste.  
4. Affichez la liste mise à jour après chaque emprunt.

---

### **Exercice 5 : Création de fonctions** (20 points)  
1. Implémentez une fonction `CalculerDateRetour` qui prend en paramètre :  
   - La durée de l'emprunt en jours.  
   - Et retourne la date de retour prévue en ajoutant cette durée à la date actuelle.  

2. Appelez cette fonction pour afficher la date de retour prévue pour une durée d'emprunt de 10 jours.

---

### **Exercice 6 : Mise en application complète** (30 points)  
Créez un programme complet en combinant les exercices précédents :  
1. Demandez à l'utilisateur de saisir :  
   - Son nom.  
   - Le titre du livre qu'il souhaite emprunter.  
   - La durée de l'emprunt (en jours).  

2. Validez les données saisies avec des boucles et conditions appropriées.  
3. Réduisez le nombre total de livres disponibles après un emprunt.  
4. Ajoutez le titre emprunté à une liste de livres empruntés.  
5. Affichez un résumé à la fin :  
   - Nom de l'emprunteur.  
   - Titre du livre emprunté.  
   - Durée de l'emprunt.  
   - Date de retour prévue.  
   - Nombre total de livres restants.

Exemple de sortie :  
```
Nom de l'emprunteur : Marie  
Livre emprunté : Le Petit Prince  
Durée de l'emprunt : 14 jours  
Date de retour prévue : 2024-12-23  
Livres restants : 99
```

---

### **Barème total : 100 points**  
- Variables : 5 points  
- Conditions : 10 points  
- Boucles : 15 points  
- Tableaux et listes : 20 points  
- Fonctions : 20 points  
- Mise en application complète : 30 points  

---
