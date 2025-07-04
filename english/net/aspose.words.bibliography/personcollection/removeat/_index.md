---
title: PersonCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words for .NET
description: Effortlessly use the PersonCollection RemoveAt method to delete a person by index, streamlining your data management with ease and precision.
type: docs
weight: 80
url: /net/aspose.words.bibliography/personcollection/removeat/
---
## PersonCollection.RemoveAt method

Removes the person at the specified index.

```csharp
public void RemoveAt(int index)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | Int32 | The zero-based index of the person to remove. |

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

* class [PersonCollection](../)
* namespace [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* assembly [Aspose.Words](../../../)
