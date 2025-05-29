---
title: VerticalAlignment Enum
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.VerticalAlignment-uppräkningen för exakt vertikal justering av textramar och tabeller i dina dokument. Förbättra layoutkontrollen!
type: docs
weight: 1790
url: /sv/net/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enumeration

Anger vertikal justering av en flytande form, textram eller en flytande tabell.

```csharp
public enum VerticalAlignment
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Objektet positioneras explicit, vanligtvis med hjälp av dess**Bästa** egendom. |
| Top | `1` | Anger att objektet ska vara högst upp på den vertikala justeringsbasen. |
| Center | `2` | Anger att objektet ska centreras i förhållande till den vertikala justeringsbasen. |
| Bottom | `3` | Anger att objektet ska vara längst ner på den vertikala justeringsbasen. |
| Inside | `4` | Anger att objektet ska vara innanför den horisontella justeringsbasen. |
| Outside | `5` | Anger att objektet ska vara utanför den vertikala justeringsbasen. |
| Inline | `-1` | Inte dokumenterat. Verkar vara ett möjligt värde för flytande stycken och tabeller. |
| Default | `0` | Samma somNone . |

## Exempel

Visar hur man infogar en flytande bild i mitten av en sida.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en flytande bild som visas bakom den överlappande texten och justera den mot sidans mitt.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### Se även

* property [VerticalAlignment](../shapebase/verticalalignment/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
