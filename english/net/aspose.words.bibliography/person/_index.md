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

## Methods

| Name | Description |
| --- | --- |
| override [Equals](../../aspose.words.bibliography/person/equals/#equals_1)(*object*) |  |
| [Equals](../../aspose.words.bibliography/person/equals/#equals)(*Person*) |  |
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
