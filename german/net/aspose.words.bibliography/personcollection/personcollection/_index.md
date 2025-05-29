---
title: PersonCollection
linktitle: PersonCollection
articleTitle: PersonCollection
second_title: Aspose.Words für .NET
description: Erstellen und verwalten Sie eine dynamische Personensammlung mit der Klasse PersonCollection. Vereinfachen Sie Ihre Datenverwaltung und verbessern Sie Ihre Anwendungen noch heute!
type: docs
weight: 10
url: /de/net/aspose.words.bibliography/personcollection/personcollection/
---
## PersonCollection() {#constructor}

Initialisieren Sie eine neue Instanz des[`PersonCollection`](../) Klasse.

```csharp
public PersonCollection()
```

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

---

## PersonCollection(*IEnumerable&lt;Person&gt;*) {#constructor_2}

```csharp
public PersonCollection(IEnumerable<Person> persons)
```

### Siehe auch

* class [Person](../../person/)
* class [PersonCollection](../)
* namensraum [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* Montage [Aspose.Words](../../../)

---

## PersonCollection(*params Person[]*) {#constructor_1}

Initialisieren Sie eine neue Instanz des[`PersonCollection`](../) Klasse.

```csharp
public PersonCollection(params Person[] persons)
```

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
