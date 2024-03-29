---
title: Font.EmphasisMark
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words for .NET
description: Font EmphasisMark property. Gets or sets the emphasis mark applied to this formatting in C#.
type: docs
weight: 110
url: /net/aspose.words/font/emphasismark/
---
## Font.EmphasisMark property

Gets or sets the emphasis mark applied to this formatting.

```csharp
public EmphasisMark EmphasisMark { get; set; }
```

## Examples

Shows how to add additional character rendered above/below the glyph-character.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Possible types of emphasis mark:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder.Font.EmphasisMark = emphasisMark; 

builder.Write("Emphasis text");
builder.Writeln();
builder.Font.ClearFormatting();
builder.Write("Simple text");

builder.Document.Save(ArtifactsDir + "Fonts.SetEmphasisMark.docx");
```

### See Also

* enum [EmphasisMark](../../emphasismark/)
* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
