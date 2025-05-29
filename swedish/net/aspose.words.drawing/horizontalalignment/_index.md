---
title: HorizontalAlignment Enum
linktitle: HorizontalAlignment
articleTitle: HorizontalAlignment
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.HorizontalAlignment-uppräkningen för exakt kontroll över horisontell justering i flytande textramar och tabeller. Förbättra din dokumentlayout!
type: docs
weight: 1360
url: /sv/net/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enumeration

Anger horisontell justering av en flytande form, textram eller flytande tabell.

```csharp
public enum HorizontalAlignment
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Objektet positioneras explicit, vanligtvis med hjälp av dess**Vänster** egendom. |
| Default | `0` | Samma somNone . |
| Left | `1` | Anger att objektet ska vänsterjusteras mot den horisontella justeringsbasen. |
| Center | `2` | Anger att objektet ska centreras i förhållande till den horisontella justeringsbasen. |
| Right | `3` | Anger att objektet ska högerjusteras i förhållande till den horisontella justeringsbasen. |
| Inside | `4` | Anger att objektet ska vara innanför den horisontella justeringsbasen. |
| Outside | `5` | Anger att objektet ska vara utanför den horisontella justeringsbasen. |

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

* property [HorizontalAlignment](../shapebase/horizontalalignment/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
