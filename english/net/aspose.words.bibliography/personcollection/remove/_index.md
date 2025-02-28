---
title: PersonCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: Effortlessly remove a person from your collection with the PersonCollection Remove method. Streamline your data management today!
type: docs
weight: 70
url: /net/aspose.words.bibliography/personcollection/remove/
---
## PersonCollection.Remove method

Removes the person from the collection.

```csharp
public bool Remove(Person person)
```

| Parameter | Type | Description |
| --- | --- | --- |
| person | Person | The person to remove from the collection. |

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
