---
title: RelativeHorizontalPosition Enum
linktitle: RelativeHorizontalPosition
articleTitle: RelativeHorizontalPosition
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.RelativeHorizontalPosition-uppräkningen för att definiera exakt horisontell positionering för former och textramar i dina dokument.
type: docs
weight: 1580
url: /sv/net/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enumeration

Anger vad den horisontella positionen för en form eller textram är relativ till.

```csharp
public enum RelativeHorizontalPosition
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Margin | `0` | Anger att den horisontella positioneringen ska vara relativ till sidmarginalerna. |
| Page | `1` | Objektet är placerat i förhållande till sidans vänstra kant. |
| Column | `2` | Objektet är placerat i förhållande till kolumnens vänstra sida. |
| Character | `3` | Objektet är placerat i förhållande till styckets vänstra sida. |
| LeftMargin | `4` | Anger att den horisontella positioneringen ska vara relativ till sidans vänstra marginal. |
| RightMargin | `5` | Anger att den horisontella positioneringen ska vara i förhållande till sidans högra marginal. |
| InsideMargin | `6` | Anger att den horisontella positioneringen ska vara relativ till den inre marginalen på den aktuella sidan (vänstermarginalen på udda sidor, högermarginalen på jämna sidor). |
| OutsideMargin | `7` | Anger att den horisontella positioneringen ska vara relativ till den yttre marginalen på den aktuella sidan (högermarginalen på udda sidor, vänstermarginalen på jämna sidor). |
| Default | `2` | Standardvärdet ärColumn . |

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

Visar hur man infogar en bild och använder den som vattenstämpel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga bilden i sidhuvudet så att den syns på varje sida.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Placera bilden i mitten av sidan.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

### Se även

* property [RelativeHorizontalPosition](../shapebase/relativehorizontalposition/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
