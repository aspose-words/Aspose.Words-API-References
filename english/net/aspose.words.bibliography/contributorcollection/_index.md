---
title: ContributorCollection Class
linktitle: ContributorCollection
articleTitle: ContributorCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Bibliography.ContributorCollection class. Represents bibliography source contributors in C#.
type: docs
weight: 50
url: /net/aspose.words.bibliography/contributorcollection/
---
## ContributorCollection class

Represents bibliography source contributors.

```csharp
public sealed class ContributorCollection : IEnumerable<Contributor>
```

## Properties

| Name | Description |
| --- | --- |
| [Artist](../../aspose.words.bibliography/contributorcollection/artist/) { get; } | Gets the artist of a source. |
| [Author](../../aspose.words.bibliography/contributorcollection/author/) { get; } | Gets the author of a source. |
| [BookAuthor](../../aspose.words.bibliography/contributorcollection/bookauthor/) { get; } | Gets the book author of a source. |
| [Compiler](../../aspose.words.bibliography/contributorcollection/compiler/) { get; } | Gets the compiler of a source. |
| [Composer](../../aspose.words.bibliography/contributorcollection/composer/) { get; } | Gets the composer of a source. |
| [Conductor](../../aspose.words.bibliography/contributorcollection/conductor/) { get; } | Gets the conductor of a source. |
| [Counsel](../../aspose.words.bibliography/contributorcollection/counsel/) { get; } | Gets the counsel of a source. |
| [Director](../../aspose.words.bibliography/contributorcollection/director/) { get; } | Gets the director of a source. |
| [Editor](../../aspose.words.bibliography/contributorcollection/editor/) { get; } | Gets the editor of a source. |
| [Interviewee](../../aspose.words.bibliography/contributorcollection/interviewee/) { get; } | Gets the interviewee of a source. |
| [Interviewer](../../aspose.words.bibliography/contributorcollection/interviewer/) { get; } | Gets the interviewer of a source. |
| [Inventor](../../aspose.words.bibliography/contributorcollection/inventor/) { get; } | Gets the inventor of a source. |
| [Performer](../../aspose.words.bibliography/contributorcollection/performer/) { get; } | Gets the performer of a source. |
| [Producer](../../aspose.words.bibliography/contributorcollection/producer/) { get; } | Gets the producer of a source. |
| [Translator](../../aspose.words.bibliography/contributorcollection/translator/) { get; } | Gets the translator of a source. |
| [Writer](../../aspose.words.bibliography/contributorcollection/writer/) { get; } | Gets the writer of a source. |

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

* class [Contributor](../contributor/)
* namespace [Aspose.Words.Bibliography](../../aspose.words.bibliography/)
* assembly [Aspose.Words](../../)
