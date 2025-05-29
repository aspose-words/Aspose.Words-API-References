---
title: ImageData.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ImageData Borders för att förbättra inbäddade bilder med anpassningsbara ramar. Förhöj dina visuella effekter och förbättra användarengagemang idag!
type: docs
weight: 20
url: /sv/net/aspose.words.drawing/imagedata/borders/
---
## ImageData.Borders property

Hämtar en samling av bildens ramar. Ramar har endast effekt för inbäddade bilder.

```csharp
public BorderCollection Borders { get; }
```

## Exempel

Visar hur man redigerar en forms bilddata.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape sourceShape = (Shape)imgSourceDoc.GetChildNodes(NodeType.Shape, true)[0];

Document dstDoc = new Document();

// Importera en form från källdokumentet och lägg till den i första stycket.
Shape importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

// Den importerade formen innehåller en bild. Vi kan komma åt bildens egenskaper och rådata via ImageData-objektet.
ImageData imageData = importedShape.ImageData;
imageData.Title = "Imported Image";

Assert.True(imageData.HasImage);

// Om en bild inte har några ramar, kommer dess ImageData-objekt att definiera ramfärgen som tom.
Assert.AreEqual(4, imageData.Borders.Count);
Assert.AreEqual(Color.Empty, imageData.Borders[0].Color);

// Den här bilden länkar inte till en annan form eller bildfil i det lokala filsystemet.
Assert.False(imageData.IsLink);
Assert.False(imageData.IsLinkOnly);

// Egenskaperna "Ljusstyrka" och "Kontrast" definierar bildens ljusstyrka och kontrast
// på en skala från 0 till 1, med standardvärdet 0,5.
imageData.Brightness = 0.8;
imageData.Contrast = 1.0;

// Ovanstående ljusstyrka- och kontrastvärden har skapat en bild med mycket vitt.
// Vi kan välja en färg med ChromaKey-egenskapen för att ersätta med transparens, till exempel vit.
imageData.ChromaKey = Color.White;

// Importera källformen igen och ställ in bilden till monokrom.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.GrayScale = true;

// Importera källformen igen för att skapa en tredje bild och ställ in den på BiLevel.
// BiLevel ställer in varje pixel till antingen svart eller vit, beroende på vilket som är närmast den ursprungliga färgen.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.BiLevel = true;

// Beskärning bestäms på en skala från 0 till 1. Beskärning av en sida med 0,3
// kommer att beskära 30% av bilden vid den beskurna sidan.
importedShape.ImageData.CropBottom = 0.3;
importedShape.ImageData.CropLeft = 0.3;
importedShape.ImageData.CropTop = 0.3;
importedShape.ImageData.CropRight = 0.3;

dstDoc.Save(ArtifactsDir + "Drawing.ImageData.docx");
```

### Se även

* class [BorderCollection](../../../aspose.words/bordercollection/)
* class [ImageData](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
