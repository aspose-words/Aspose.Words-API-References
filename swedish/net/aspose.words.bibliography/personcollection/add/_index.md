---
title: PersonCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words för .NET
description: Lägg enkelt till en person i din samling med PersonCollection Add-metoden. Effektivisera datahanteringen och förbättra ditt projekts effektivitet!
type: docs
weight: 40
url: /sv/net/aspose.words.bibliography/personcollection/add/
---
## PersonCollection.Add method

Lägger till en[`Person`](../../person/) till samlingen.

```csharp
public void Add(Person person)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| person | Person | Personen som ska läggas till i samlingen. |

## Exempel

Visar hur man arbetar med personinsamling.

```csharp
// Skapa en ny personsamling.
PersonCollection persons = new PersonCollection();
Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
// Lägg till ny person i samlingen.
persons.Add(person);
Assert.AreEqual(1, persons.Count);
// Ta bort personen från samlingen om den finns.
if (persons.Contains(person))
    persons.Remove(person);
Assert.AreEqual(0, persons.Count);

// Skapa personsamling med två personer.
persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
Assert.AreEqual(2, persons.Count);
// Ta bort person från samlingen via index.
persons.RemoveAt(0);
Assert.AreEqual(1, persons.Count);
// Ta bort alla personer från samlingen.
persons.Clear();
Assert.AreEqual(0, persons.Count);
```

### Se även

* class [Person](../../person/)
* class [PersonCollection](../)
* namnutrymme [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* hopsättning [Aspose.Words](../../../)
