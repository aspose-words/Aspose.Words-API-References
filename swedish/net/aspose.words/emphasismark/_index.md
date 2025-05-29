---
title: EmphasisMark Enum
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.EmphasisMark enum, med olika betoningstyper för att förbättra formateringen av ditt dokument. Öka din texts effekt idag!
type: docs
weight: 1870
url: /sv/net/aspose.words/emphasismark/
---
## EmphasisMark enumeration

Anger möjliga typer av betoningstecken.

```csharp
public enum EmphasisMark
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Inget betoningstecken. |
| OverSolidCircle | `1` | Betoningstecken är en heldragen svart cirkel som visas ovanför texten. |
| OverComma | `2` | Betoningstecken är ett kommatecken som visas ovanför text. |
| OverWhiteCircle | `3` | Betoningstecken är en tom vit cirkel som visas ovanför texten. |
| UnderSolidCircle | `4` | Betoningstecken är en heldragen svart cirkel som visas under texten. |

## Exempel

Visar hur man lägger till ytterligare tecken som renderas ovanför/under tecknet.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Möjliga typer av betoningstecken:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder.Font.EmphasisMark = emphasisMark; 

builder.Write("Emphasis text");
builder.Writeln();
builder.Font.ClearFormatting();
builder.Write("Simple text");

builder.Document.Save(ArtifactsDir + "Fonts.SetEmphasisMark.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
