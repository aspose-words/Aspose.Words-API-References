---
title: WrapType Enum
linktitle: WrapType
articleTitle: WrapType
second_title: Aspose.Words för .NET
description: Aspose.Words.Drawing.WrapType uppräkning. Anger hur text lindas runt en form eller bild i C#.
type: docs
weight: 1400
url: /sv/net/aspose.words.drawing/wraptype/
---
## WrapType enumeration

Anger hur text lindas runt en form eller bild.

```csharp
public enum WrapType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `3` | Ingen textlindning runt formen. Formen placeras bakom eller framför text. |
| Inline | `0` | Formen förblir på samma lager som text och behandlas som ett tecken. |
| TopBottom | `1` | Texten stannar överst i formen och startar om på raden under formen. |
| Square | `2` | Lindar text runt alla sidor av den fyrkantiga begränsningsrutan för formen. |
| Tight | `4` | Lindas tätt runt kanterna på formen, istället för att svepa runt begränsningsrutan. |
| Through | `5` | Samma som Tight, men lindas inuti alla delar av formen som är öppna. |

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

Visar hur man infogar en bild och använder den som vattenstämpel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga bilden i rubriken så att den syns på varje sida.
Image image = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(image);
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Placera bilden i mitten av sidan.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

Visar hur man infogar en bild och använder den som vattenstämpel (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga bilden i rubriken så att den syns på varje sida.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

using (SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png"))
{
    builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
    Shape shape = builder.InsertImage(image);
    shape.WrapType = WrapType.None;
    shape.BehindText = true;

    // Placera bilden i mitten av sidan.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
    shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
    shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
    shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermarkNetStandard2.docx");
```

### Se även

* property [WrapType](../shapebase/wraptype/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
