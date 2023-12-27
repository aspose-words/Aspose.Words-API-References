---
title: Bibliography.Sources
linktitle: Sources
articleTitle: Sources
second_title: Aspose.Words for .NET
description: Bibliography Sources property. Gets a collection that represents all the sources contained in a bibliography in C#.
type: docs
weight: 20
url: /net/aspose.words.bibliography/bibliography/sources/
---
## Bibliography.Sources property

Gets a collection that represents all the sources contained in a bibliography.

```csharp
public ICollection<Source> Sources { get; }
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

* class [Source](../../source/)
* class [Bibliography](../)
* namespace [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* assembly [Aspose.Words](../../../)
