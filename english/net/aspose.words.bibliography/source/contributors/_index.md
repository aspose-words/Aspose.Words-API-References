---
title: Source.Contributors
linktitle: Contributors
articleTitle: Contributors
second_title: Aspose.Words for .NET
description: Source Contributors property. Gets contributors list author editor writer etc of a source in C#.
type: docs
weight: 110
url: /net/aspose.words.bibliography/source/contributors/
---
## Source.Contributors property

Gets contributors list (author, editor, writer etc) of a source.

```csharp
public ContributorCollection Contributors { get; }
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

* class [ContributorCollection](../../contributorcollection/)
* class [Source](../)
* namespace [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* assembly [Aspose.Words](../../../)
