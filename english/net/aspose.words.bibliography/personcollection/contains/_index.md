---
title: PersonCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words for .NET
description: Discover if a PersonCollection includes a specific individual with our efficient Contains method. Simplify your data management today!
type: docs
weight: 60
url: /net/aspose.words.bibliography/personcollection/contains/
---
## PersonCollection.Contains method

Determines whether the collection contains a specific person.

```csharp
public bool Contains(Person person)
```

| Parameter | Type | Description |
| --- | --- | --- |
| person | Person | The person to locate in the collection. |

## Examples

Shows how to work with person collection.

```csharp
// Create a new person collection.
PersonCollection persons = new PersonCollection();
Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
// Add new person to the collection.
persons.Add(person);
Assert.AreEqual(1, persons.Count);
// Remove person from the collection if it exists.
if (persons.Contains(person))
    persons.Remove(person);
Assert.AreEqual(0, persons.Count);

// Create person collection with two persons.
persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
Assert.AreEqual(2, persons.Count);
// Remove person from the collection by the index.
persons.RemoveAt(0);
Assert.AreEqual(1, persons.Count);
// Remove all persons from the collection.
persons.Clear();
Assert.AreEqual(0, persons.Count);
```

### See Also

* class [Person](../../person/)
* class [PersonCollection](../)
* namespace [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* assembly [Aspose.Words](../../../)
