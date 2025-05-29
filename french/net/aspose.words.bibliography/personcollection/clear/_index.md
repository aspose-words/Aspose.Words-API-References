---
title: PersonCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words pour .NET
description: Effacez facilement votre collection de personnes grâce à notre méthode Clear, qui supprime instantanément tous les éléments pour un nouveau départ. Simplifiez la gestion de vos données dès aujourd'hui !
type: docs
weight: 50
url: /fr/net/aspose.words.bibliography/personcollection/clear/
---
## PersonCollection.Clear method

Supprime tous les éléments de la collection.

```csharp
public void Clear()
```

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

* class [PersonCollection](../)
* espace de noms [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* Assemblée [Aspose.Words](../../../)
