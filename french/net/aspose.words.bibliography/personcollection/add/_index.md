---
title: PersonCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words pour .NET
description: Ajoutez facilement une personne à votre collection grâce à la méthode PersonCollection Add. Simplifiez la gestion des données et optimisez l'efficacité de votre projet !
type: docs
weight: 40
url: /fr/net/aspose.words.bibliography/personcollection/add/
---
## PersonCollection.Add method

Ajoute un[`Person`](../../person/) à la collection.

```csharp
public void Add(Person person)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| person | Person | La personne à ajouter à la collection. |

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
