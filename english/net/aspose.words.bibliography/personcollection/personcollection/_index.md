---
title: PersonCollection
linktitle: PersonCollection
articleTitle: PersonCollection
second_title: Aspose.Words for .NET
description: Create and manage a dynamic collection of individuals with the PersonCollection class. Simplify your data handling and enhance your applications today!
type: docs
weight: 10
url: /net/aspose.words.bibliography/personcollection/personcollection/
---
## PersonCollection() {#constructor}

Initialize a new instance of the [`PersonCollection`](../) class.

```csharp
public PersonCollection()
```

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

---

## PersonCollection(*IEnumerable&lt;Person&gt;*) {#constructor_2}

```csharp
public PersonCollection(IEnumerable<Person> persons)
```

### See Also

* class [Person](../../person/)
* class [PersonCollection](../)
* namespace [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* assembly [Aspose.Words](../../../)

---

## PersonCollection(*params Person[]*) {#constructor_1}

Initialize a new instance of the [`PersonCollection`](../) class.

```csharp
public PersonCollection(params Person[] persons)
```

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
