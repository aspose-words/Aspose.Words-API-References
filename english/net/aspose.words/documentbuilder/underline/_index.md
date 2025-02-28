---
title: DocumentBuilder.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words for .NET
description: Discover DocumentBuilder's Underline property to easily customize font styles. Enhance your documents with versatile underline options for a professional look.
type: docs
weight: 190
url: /net/aspose.words/documentbuilder/underline/
---
## DocumentBuilder.Underline property

Gets/sets underline type for the current font.

```csharp
public Underline Underline { get; set; }
```

## Examples

Shows how to format text inserted by a document builder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Dash;
builder.Font.Color = Color.Blue;
builder.Font.Size = 32;

// The builder applies formatting to its current paragraph and any new text added by it afterward.
builder.Writeln("Large, blue, and underlined text.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertUnderline.docx");
```

### See Also

* enum [Underline](../../underline/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
