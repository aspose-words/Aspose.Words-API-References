---
title: Shape.ImageData
linktitle: ImageData
articleTitle: ImageData
second_title: Aspose.Words för .NET
description: Shape ImageData fast egendom. Ger tillgång till bilden av formen. Returnerarnull om formen inte kan ha en bild i C#.
type: docs
weight: 110
url: /sv/net/aspose.words.drawing/shape/imagedata/
---
## Shape.ImageData property

Ger tillgång till bilden av formen. Returnerar`null` om formen inte kan ha en bild.

```csharp
public ImageData ImageData { get; }
```

## Exempel

Visar hur man extraherar bilder från ett dokument och sparar dem i det lokala filsystemet som enskilda filer.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Hämta samlingen av former från dokumentet,
// och spara bilddata för varje form med en bild som en fil till det lokala filsystemet.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Bilddata för former kan innehålla bilder av många möjliga bildformat.
        // Vi kan bestämma en filtillägg för varje bild automatiskt, baserat på dess format.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Visar hur man infogar en länkad bild i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Nedan finns två sätt att applicera en bild på en form så att den kan visa den.
// 1 - Ställ in formen så att den innehåller bilden.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Varje bild som vi lagrar i form kommer att öka storleken på vårt dokument.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Ställ in formen för att länka till en bildfil i det lokala filsystemet.
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

* class [ImageData](../../imagedata/)
* class [Shape](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
