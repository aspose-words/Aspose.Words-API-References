---
title: LayoutOptions.ShowParagraphMarks
linktitle: ShowParagraphMarks
second_title: Aspose.Words for .NET API Reference
description: LayoutOptions ShowParagraphMarks property. Gets or sets indication of whether paragraph marks are rendered. Default is false in C#.
type: docs
weight: 80
url: /net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## ShowParagraphMarks property

Gets or sets indication of whether paragraph marks are rendered. Default is `false`.

```csharp
public bool ShowParagraphMarks { get; set; }
```

## Examples

Shows how to show paragraph marks in a rendered output document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Add some paragraphs, then enable paragraph marks to show the ends of paragraphs
// with a pilcrow (¶) symbol when we render the document.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

### See Also

* class [LayoutOptions](../)
* namespace [Aspose.Words.Layout](../../layoutoptions/)
* assembly [Aspose.Words](../../../)
