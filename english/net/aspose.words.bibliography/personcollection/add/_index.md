---
title: PersonCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: Effortlessly add a Person to your collection with the PersonCollection Add method. Streamline data management and enhance your project’s efficiency!
type: docs
weight: 40
url: /net/aspose.words.bibliography/personcollection/add/
---
## PersonCollection.Add method

Adds a [`Person`](../../person/) to the collection.

```csharp
public void Add(Person person)
```

| Parameter | Type | Description |
| --- | --- | --- |
| person | Person | The person to add to the collection. |

## Examples

Shows how to work with person collection.

```csharp
// Create a new person collection.
PersonCollection persons = new PersonCollection();
Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
// Add new person to the collection.
persons.Add(person);
Assert.That(persons.Count, Is.EqualTo(1));
// Remove person from the collection if it exists.
if (persons.Contains(person))
    persons.Remove(person);
Assert.That(persons.Count, Is.EqualTo(0));

// Create person collection with two persons.
persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
Assert.That(persons.Count, Is.EqualTo(2));
// Remove person from the collection by the index.
persons.RemoveAt(0);
Assert.That(persons.Count, Is.EqualTo(1));
// Remove all persons from the collection.
persons.Clear();
Assert.That(persons.Count, Is.EqualTo(0));
```

### See Also

* class [Person](../../person/)
* class [PersonCollection](../)
* namespace [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* assembly [Aspose.Words](../../../)
