---
title: FindReplaceOptions.IgnoreDeleted
linktitle: IgnoreDeleted
articleTitle: IgnoreDeleted
second_title: Aspose.Words for .NET
description: Discover the FindReplaceOptions IgnoreDeleted property, control text visibility in deleted revisions with an easy boolean toggle. Enhance your editing experience!
type: docs
weight: 60
url: /net/aspose.words.replacing/findreplaceoptions/ignoredeleted/
---
## FindReplaceOptions.IgnoreDeleted property

Gets or sets a boolean value indicating either to ignore text inside delete revisions. The default value is `false`.

```csharp
public bool IgnoreDeleted { get; set; }
```

## Examples

Shows how to include or ignore text inside delete revisions during a find-and-replace operation.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Start tracking revisions and remove the second paragraph, which will create a delete revision.
// That paragraph will persist in the document until we accept the delete revision.
doc.StartTrackRevisions("John Doe", DateTime.Now);
doc.FirstSection.Body.Paragraphs[1].Remove();
doc.StopTrackRevisions();

Assert.That(doc.FirstSection.Body.Paragraphs[1].IsDeleteRevision, Is.True);

// We can use a "FindReplaceOptions" object to modify the find and replace process.
FindReplaceOptions options = new FindReplaceOptions();

// Set the "IgnoreDeleted" flag to "true" to get the find-and-replace
// operation to ignore paragraphs that are delete revisions.
// Set the "IgnoreDeleted" flag to "false" to get the find-and-replace
// operation to also search for text inside delete revisions.
options.IgnoreDeleted = ignoreTextInsideDeleteRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.That(doc.GetText().Trim(), Is.EqualTo(ignoreTextInsideDeleteRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!"));
```

### See Also

* class [FindReplaceOptions](../)
* namespace [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assembly [Aspose.Words](../../../)
