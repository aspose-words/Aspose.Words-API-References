---
title: PersonCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words für .NET
description: Verwenden Sie mühelos die RemoveAt-Methode der PersonCollection, um eine Person nach Index zu löschen und so Ihre Datenverwaltung einfach und präzise zu optimieren.
type: docs
weight: 80
url: /de/net/aspose.words.bibliography/personcollection/removeat/
---
## PersonCollection.RemoveAt method

Entfernt die Person am angegebenen Index.

```csharp
public void RemoveAt(int index)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | Int32 | Der nullbasierte Index der zu entfernenden Person. |

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

* class [PersonCollection](../)
* namensraum [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* Montage [Aspose.Words](../../../)
