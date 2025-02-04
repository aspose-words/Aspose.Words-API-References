---
title: EmphasisMark Enum
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words for .NET
description: Aspose.Words.EmphasisMark enum. Specifies possible types of emphasis mark in C#.
type: docs
weight: 1860
url: /net/aspose.words/emphasismark/
---
## EmphasisMark enumeration

Specifies possible types of emphasis mark.

```csharp
public enum EmphasisMark
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | No emphasis mark. |
| OverSolidCircle | `1` | Emphasis mark is a solid black circle displayed above text. |
| OverComma | `2` | Emphasis mark is a comma character displayed above text. |
| OverWhiteCircle | `3` | Emphasis mark is an empty white circle displayed above text. |
| UnderSolidCircle | `4` | Emphasis mark is a solid black circle displayed below text. |

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
