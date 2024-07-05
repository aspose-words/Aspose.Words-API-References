---
title: Bibliography Class
linktitle: Bibliography
articleTitle: Bibliography
second_title: Aspose.Words for .NET
description: Aspose.Words.Bibliography.Bibliography class. Represents the list of bibliography sources available in the document in C#.
type: docs
weight: 30
url: /net/aspose.words.bibliography/bibliography/
---
## Bibliography class

Represents the list of bibliography sources available in the document.

```csharp
public sealed class Bibliography
```

## Properties

| Name | Description |
| --- | --- |
| [BibliographyStyle](../../aspose.words.bibliography/bibliography/bibliographystyle/) { get; } | Gets a string that represents the name of the active style to use for a bibliography. |
| [Sources](../../aspose.words.bibliography/bibliography/sources/) { get; } | Gets a collection that represents all the sources contained in a bibliography. |

## Examples

Shows how to get bibliography sources available in the document.

```csharp
Document document = new Document(MyDir + "Bibliography sources.docx");

Bibliography bibliography = document.Bibliography;
Assert.AreEqual(12, bibliography.Sources.Count);

Source source = bibliography.Sources.FirstOrDefault();
Assert.AreEqual("Book 0 (No LCID)", source.Title);

ContributorCollection contributors = source.Contributors;
Assert.IsNull(contributors.Artist);
Assert.IsNull(contributors.BookAuthor);
Assert.IsNull(contributors.Compiler);
Assert.IsNull(contributors.Composer);
Assert.IsNull(contributors.Conductor);
Assert.IsNull(contributors.Counsel);
Assert.IsNull(contributors.Director);
Assert.IsNotNull(contributors.Editor);
Assert.IsNull(contributors.Interviewee);
Assert.IsNull(contributors.Interviewer);
Assert.IsNull(contributors.Inventor);
Assert.IsNull(contributors.Performer);
Assert.IsNull(contributors.Producer);
Assert.IsNotNull(contributors.Translator);
Assert.IsNull(contributors.Writer);
Contributor editor  = contributors.Editor;
Assert.AreEqual(2, ((PersonCollection)editor).Count());
PersonCollection authors = (PersonCollection)contributors.Author;
Assert.AreEqual(2, authors.Count());

Person person = authors[0];
Assert.AreEqual("Roxanne", person.First);
Assert.AreEqual("Brielle", person.Middle);
Assert.AreEqual("Tejeda", person.Last);
```

### See Also

* namespace [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* assembly [Aspose.Words](../../)
