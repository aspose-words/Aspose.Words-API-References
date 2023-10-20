---
title: JustificationMode Enum
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words för .NET
description: Aspose.Words.Settings.JustificationMode uppräkning. Anger teckenavståndsjusteringen för ett dokument. Standardvärdet ärBygga ut  i C#.
type: docs
weight: 5800
url: /sv/net/aspose.words.settings/justificationmode/
---
## JustificationMode enumeration

Anger teckenavståndsjusteringen för ett dokument. Standardvärdet är`Bygga ut` .

```csharp
public enum JustificationMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Expand | `0` |  |
| Compress | `1` |  |
| CompressKana | `2` |  |

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
