---
title: PersonCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words für .NET
description: Entfernen Sie mühelos eine Person aus Ihrer Sammlung mit der Methode „PersonCollection Remove“. Optimieren Sie noch heute Ihr Datenmanagement!
type: docs
weight: 70
url: /de/net/aspose.words.bibliography/personcollection/remove/
---
## PersonCollection.Remove method

Entfernt die Person aus der Sammlung.

```csharp
public bool Remove(Person person)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| person | Person | Die Person, die aus der Sammlung entfernt werden soll. |

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
