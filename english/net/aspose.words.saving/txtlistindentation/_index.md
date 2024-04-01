---
title: TxtListIndentation Class
linktitle: TxtListIndentation
articleTitle: TxtListIndentation
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.TxtListIndentation class. Specifies how list levels are indented when document is exporting to Text format in C#.
type: docs
weight: 5830
url: /net/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class

Specifies how list levels are indented when document is exporting to Text format.

To learn more, visit the [Save a Document](https://docs.aspose.com/words/net/save-a-document/) documentation article.

```csharp
public class TxtListIndentation
```

## Constructors

| Name | Description |
| --- | --- |
| [TxtListIndentation](txtlistindentation/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [Character](../../aspose.words.saving/txtlistindentation/character/) { get; set; } | Gets or sets which character to use for indenting list levels. The default value is '\0', that means there is no indentation. |
| [Count](../../aspose.words.saving/txtlistindentation/count/) { get; set; } | Gets or sets how many [`Character`](./character/) to use as indentation per one list level. The default value is 0, that means no indentation. |

## Examples

Shows how to configure list indenting when saving a document to plaintext.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Create a list with three levels of indentation.
builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent(); 
builder.Write("Item 3");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Set the "Character" property to assign a character to use
// for padding that simulates list indentation in plaintext.
txtSaveOptions.ListIndentation.Character = ' ';

// Set the "Count" property to specify the number of times
// to place the padding character for each list indent level.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");

Assert.AreEqual("1. Item 1\r\n" +
                "   a. Item 2\r\n" +
                "      i. Item 3\r\n", docText);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
