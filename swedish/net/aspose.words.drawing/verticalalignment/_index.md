---
title: Enum VerticalAlignment
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Drawing.VerticalAlignment uppräkning. Anger vertikal justering av en flytande form textram eller en flytande tabell.
type: docs
weight: 1230
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
| None | `0` | Objektet är explicit positionerat, vanligtvis med hjälp av dess **Topp** egenskap. |
| Top | `1` | Anger att objektet ska vara överst på den vertikala inriktningsbasen. |
| Center | `2` | Anger att objektet ska centreras med avseende på den vertikala inriktningsbasen. |
| Bottom | `3` | Anger att objektet ska vara längst ner på den vertikala inriktningsbasen. |
| Inside | `4` | Anger att objektet ska vara inuti den horisontella inriktningsbasen. |
| Outside | `5` | Anger att objektet ska vara utanför den vertikala inriktningsbasen. |
| Inline | `-1` | Ej dokumenterat. Verkar vara ett möjligt värde för flytande stycken och tabeller. |
| Default | `0` | Samma somNone . |

### Exempel

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

* property [VerticalAlignment](../shapebase/verticalalignment/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)


