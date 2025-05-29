---
title: PersonCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words pour .NET
description: Découvrez si une PersonCollection inclut un individu spécifique grâce à notre méthode efficace « Contenu ». Simplifiez la gestion de vos données dès aujourd'hui !
type: docs
weight: 60
url: /fr/net/aspose.words.bibliography/personcollection/contains/
---
## PersonCollection.Contains method

Détermine si la collection contient une personne spécifique.

```csharp
public bool Contains(Person person)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| person | Person | La personne à localiser dans la collection. |

## Exemples

Montre comment travailler avec la collection de personnes.

```csharp
// Créer une nouvelle collection de personnes.
PersonCollection persons = new PersonCollection();
Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
// Ajouter une nouvelle personne à la collection.
persons.Add(person);
Assert.AreEqual(1, persons.Count);
// Supprimer la personne de la collection si elle existe.
if (persons.Contains(person))
    persons.Remove(person);
Assert.AreEqual(0, persons.Count);

// Créer une collection de personnes avec deux personnes.
persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
Assert.AreEqual(2, persons.Count);
// Supprimer la personne de la collection par l'index.
persons.RemoveAt(0);
Assert.AreEqual(1, persons.Count);
// Supprimer toutes les personnes de la collection.
persons.Clear();
Assert.AreEqual(0, persons.Count);
```

### Voir également

* class [Person](../../person/)
* class [PersonCollection](../)
* espace de noms [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* Assemblée [Aspose.Words](../../../)
