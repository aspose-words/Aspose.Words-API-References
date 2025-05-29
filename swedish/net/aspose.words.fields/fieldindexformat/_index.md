---
title: FieldIndexFormat Enum
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.FieldIndexFormat-enum för anpassningsbar FieldIndex-formatering i dina dokument. Förbättra dokumentstrukturen utan ansträngning!
type: docs
weight: 2480
url: /sv/net/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enumeration

Anger formateringen för[`FieldIndex`](../fieldindex/) fält i ett dokument.

```csharp
public enum FieldIndexFormat
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Template | `0` | Från mall. |
| Classic | `1` | Klassisk. |
| Fancy | `2` | Lust. |
| Modern | `3` | Modern. |
| Bulleted | `4` | Punktmarkerad. |
| Formal | `5` | Formell. |
| Simple | `6` | Enkel. |

## Exempel

Visar hur man formaterar FieldIndex-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("A");
builder.InsertBreak(BreakType.LineBreak);
builder.InsertField("XE \"A\"");
builder.Write("B");

builder.InsertField(" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", null);

doc.FieldOptions.FieldIndexFormat = FieldIndexFormat.Fancy;
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.SetFieldIndexFormat.docx");
```

### Se även

* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
