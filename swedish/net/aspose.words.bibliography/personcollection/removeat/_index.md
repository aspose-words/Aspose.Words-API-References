---
title: PersonCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words för .NET
description: Använd enkelt PersonCollection RemoveAt-metoden för att ta bort en person via index, vilket effektiviserar din datahantering med enkelhet och precision.
type: docs
weight: 80
url: /sv/net/aspose.words.bibliography/personcollection/removeat/
---
## PersonCollection.RemoveAt method

Tar bort personen vid det angivna indexet.

```csharp
public void RemoveAt(int index)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | Int32 | Det nollbaserade indexet för den person som ska tas bort. |

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

* class [PersonCollection](../)
* namnutrymme [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* hopsättning [Aspose.Words](../../../)
