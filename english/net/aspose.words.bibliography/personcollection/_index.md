---
title: PersonCollection Class
linktitle: PersonCollection
articleTitle: PersonCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Bibliography.PersonCollection class. Represents a list of persons who are bibliography source contributors in C#.
type: docs
weight: 80
url: /net/aspose.words.bibliography/personcollection/
---
## PersonCollection class

Represents a list of persons who are bibliography source contributors.

```csharp
public sealed class PersonCollection : Contributor, IEnumerable<Person>
```

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

* class [Contributor](../contributor/)
* class [Person](../person/)
* namespace [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* assembly [Aspose.Words](../../)
