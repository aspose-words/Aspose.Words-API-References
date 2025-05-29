---
title: JustificationMode Enum
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words JustificationMode-enum för exakta justeringar av teckenavstånd i dina dokument. Förbättra läsbarheten med anpassningsbara inställningar!
type: docs
weight: 6630
url: /sv/net/aspose.words.settings/justificationmode/
---
## JustificationMode enumeration

Anger justeringen av teckenavståndet för ett dokument. Standardvärdet är`Expandera` .

```csharp
public enum JustificationMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Expand | `0` | Komprimera inte teckenavståndet. |
| Compress | `1` | Komprimera teckenavstånd. |
| CompressKana | `2` | Komprimera med hjälp av reglerna för kana-stavelserna, Hiragana och Katakana. |

## Exempel

Visar hur man hanterar teckenavståndskontroll.

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### Se även

* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)
