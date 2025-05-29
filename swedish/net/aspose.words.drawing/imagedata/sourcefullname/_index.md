---
title: ImageData.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ImageData SourceFullName för att enkelt hantera länkade bildsökvägar och filnamn, vilket förbättrar din bildhanteringseffektivitet.
type: docs
weight: 170
url: /sv/net/aspose.words.drawing/imagedata/sourcefullname/
---
## ImageData.SourceFullName property

Hämtar eller anger sökvägen och namnet på källfilen för den länkade bilden.

```csharp
public string SourceFullName { get; set; }
```

## Anmärkningar

Standardvärdet är en tom sträng.

Om`SourceFullName` inte är en tom sträng, bilden är länkad.

## Exempel

Visar hur man infogar en länkad bild i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Nedan följer två sätt att tillämpa en bild på en form så att den kan visas.
// 1 - Ange formen så att den innehåller bilden.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Varje bild som vi lagrar i form kommer att öka storleken på vårt dokument.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Ange formen för att länka till en bildfil i det lokala filsystemet.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Att länka till bilder sparar utrymme och resulterar i ett mindre dokument.
// Dokumentet kan dock bara visa bilden korrekt medan
// bildfilen finns på den plats som formens "SourceFullName"-egenskap pekar på.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Se även

* class [ImageData](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
