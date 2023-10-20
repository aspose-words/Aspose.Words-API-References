---
title: HorizontalAlignment Enum
linktitle: HorizontalAlignment
articleTitle: HorizontalAlignment
second_title: Aspose.Words för .NET
description: Aspose.Words.Drawing.HorizontalAlignment uppräkning. Anger horisontell justering av en flytande form textram eller flytande tabell i C#.
type: docs
weight: 1030
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
| None | `0` | Objektet är explicit positionerat, vanligtvis med hjälp av dess**Vänster** egenskap. |
| Default | `0` | Samma somNone . |
| Left | `1` | Anger att objektet ska lämnas justerat till den horisontella inriktningsbasen. |
| Center | `2` | Anger att objektet ska centreras med avseende på den horisontella inriktningsbasen. |
| Right | `3` | Anger att objektet ska vara högerjusterat mot den horisontella inriktningsbasen. |
| Inside | `4` | Anger att objektet ska vara inuti den horisontella inriktningsbasen. |
| Outside | `5` | Anger att objektet ska vara utanför den horisontella inriktningsbasen. |

## Exempel

Visar hur man infogar en flytande bild i mitten av en sida.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en flytande bild som kommer att visas bakom den överlappande texten och justera den mot sidans mitt.
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
