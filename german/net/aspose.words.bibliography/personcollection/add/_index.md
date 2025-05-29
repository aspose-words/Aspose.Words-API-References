---
title: PersonCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words für .NET
description: Fügen Sie Ihrer Sammlung mühelos eine Person mit der Methode „PersonCollection Add“ hinzu. Optimieren Sie die Datenverwaltung und steigern Sie die Effizienz Ihres Projekts!
type: docs
weight: 40
url: /de/net/aspose.words.bibliography/personcollection/add/
---
## PersonCollection.Add method

Fügt ein[`Person`](../../person/) zur Sammlung.

```csharp
public void Add(Person person)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| person | Person | Die Person, die der Sammlung hinzugefügt werden soll. |

## Beispiele

Zeigt, wie mit der Personensammlung gearbeitet wird.

```csharp
// Erstellen Sie eine neue Personensammlung.
PersonCollection persons = new PersonCollection();
Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
// Neue Person zur Sammlung hinzufügen.
persons.Add(person);
Assert.AreEqual(1, persons.Count);
// Person aus der Sammlung entfernen, falls vorhanden.
if (persons.Contains(person))
    persons.Remove(person);
Assert.AreEqual(0, persons.Count);

// Personensammlung mit zwei Personen erstellen.
persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
Assert.AreEqual(2, persons.Count);
// Person anhand des Index aus der Sammlung entfernen.
persons.RemoveAt(0);
Assert.AreEqual(1, persons.Count);
// Alle Personen aus der Sammlung entfernen.
persons.Clear();
Assert.AreEqual(0, persons.Count);
```

### Siehe auch

* class [Person](../../person/)
* class [PersonCollection](../)
* namensraum [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* Montage [Aspose.Words](../../../)
