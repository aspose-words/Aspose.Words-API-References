---
title: PersonCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words for .NET
description: Effortlessly clear your PersonCollection with our Clear method, instantly removing all items for a fresh start. Simplify your data management today!
type: docs
weight: 50
url: /net/aspose.words.bibliography/personcollection/clear/
---
## PersonCollection.Clear method

Removes all items from the collection.

```csharp
public void Clear()
```

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

* class [PersonCollection](../)
* namespace [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* assembly [Aspose.Words](../../../)
