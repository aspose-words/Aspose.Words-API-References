---
title: PageSetup.PageHeight
linktitle: PageHeight
articleTitle: PageHeight
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PageSetup PageHeight för att effektivt hantera dokumentets höjd i punkter, vilket förbättrar din layout och presentation.
type: docs
weight: 310
url: /sv/net/aspose.words/pagesetup/pageheight/
---
## PageSetup.PageHeight property

Returnerar eller anger sidans höjd i punkter.

```csharp
public double PageHeight { get; set; }
```

## Exempel

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

* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
