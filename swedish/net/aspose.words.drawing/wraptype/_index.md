---
title: WrapType Enum
linktitle: WrapType
articleTitle: WrapType
second_title: Aspose.Words för .NET
description: Upptäck hur Aspose.Words.Drawing.WrapType-enum förbättrar textbrytning runt former och bilder för professionell dokumentformatering.
type: docs
weight: 1810
url: /sv/net/aspose.words.drawing/wraptype/
---
## WrapType enumeration

Anger hur text radbryts runt en form eller bild.

```csharp
public enum WrapType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `3` | Ingen textradbrytning runt formen. Formen placeras bakom eller framför texten. |
| Inline | `0` | Formen finns kvar på samma lager som text och behandlas som ett tecken. |
| TopBottom | `1` | Texten stannar högst upp i formen och börjar om på raden under formen. |
| Square | `2` | Radbryter text runt alla sidor av den fyrkantiga avgränsningsramen för formen. |
| Tight | `4` | Omsluter tätt runt formens kanter istället för att omsluta avgränsningsramen. |
| Through | `5` | Samma som Tight, men omsluter alla öppna delar av formen. |

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

* property [WrapType](../shapebase/wraptype/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
