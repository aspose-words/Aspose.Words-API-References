---
title: Person Class
linktitle: Person
articleTitle: Person
second_title: Aspose.Words for .NET
description: Aspose.Words.Bibliography.Person class. Represents individual a person bibliography source contributor in C#.
type: docs
weight: 70
url: /net/aspose.words.bibliography/person/
---
## Person class

Represents individual (a person) bibliography source contributor.

```csharp
public sealed class Person
```

## Properties

| Name | Description |
| --- | --- |
| [First](../../aspose.words.bibliography/person/first/) { get; } | Gets the first name of a person. |
| [Last](../../aspose.words.bibliography/person/last/) { get; } | Gets the last name of a person. |
| [Middle](../../aspose.words.bibliography/person/middle/) { get; } | Gets the middle name of a person. |

## Methods

| Name | Description |
| --- | --- |
| override [Equals](../../aspose.words.bibliography/person/equals/)(*object*) |  |
| override [GetHashCode](../../aspose.words.bibliography/person/gethashcode/)() |  |

## Examples

Shows how to get bibliography sources available in the document.

```csharp
Document document = new Document(MyDir + "Bibliography sources.docx");

Bibliography bibliography = document.Bibliography;
Assert.AreEqual(12, bibliography.Sources.Count);

Source source = bibliography.Sources.FirstOrDefault();
Assert.AreEqual("Book 0 (No LCID)", source.Title);

ContributorCollection contributors = source.Contributors;
PersonCollection authors = (PersonCollection)contributors.Author;
Assert.AreEqual(2, authors.Count());

Person person = authors.FirstOrDefault();
Assert.AreEqual("Roxanne", person.First);
Assert.AreEqual("Brielle", person.Middle);
Assert.AreEqual("Tejeda", person.Last);
```

### See Also

* namespace [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* assembly [Aspose.Words](../../)
