---
title: ImageData
second_title: Aspose.Words för .NET API Referens
description: Definierar en bild för en form.
type: docs
weight: 930
url: /sv/net/aspose.words.drawing/imagedata/
---
## ImageData class

Definierar en bild för en form.

```csharp
public class ImageData
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel/) { get; set; } | Bestämmer om en bild ska visas i svartvitt. |
| [Borders](../../aspose.words.drawing/imagedata/borders/) { get; } | Hämtar samlingen av kanter för bilden. Kanter har endast effekt för inline-bilder. |
| [Brightness](../../aspose.words.drawing/imagedata/brightness/) { get; set; } | Hämtar eller ställer in bildens ljusstyrka. Värdet för den här egenskapen måste vara ett tal från 0,0 (dynast) till 1,0 (ljusast). |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey/) { get; set; } | Definierar färgvärdet för bilden som kommer att behandlas som transparent. |
| [Contrast](../../aspose.words.drawing/imagedata/contrast/) { get; set; } | Hämtar eller ställer in kontrasten för den angivna bilden. Värdet för den här egenskapen måste vara ett tal från 0,0 (den minsta kontrasten) till 1,0 (den största kontrasten). |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom/) { get; set; } | Definierar andelen av bildborttagning från undersidan. |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft/) { get; set; } | Definierar andelen av bildborttagning från vänster sida. |
| [CropRight](../../aspose.words.drawing/imagedata/cropright/) { get; set; } | Definierar andelen av bildborttagning från höger sida. |
| [CropTop](../../aspose.words.drawing/imagedata/croptop/) { get; set; } | Definierar andelen av bildborttagning från ovansidan. |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale/) { get; set; } | Bestämmer om en bild ska visas i gråskaleläge. |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage/) { get; } | Returnerar sant om formen har bildbytes eller länkar en bild. |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes/) { get; set; } | Hämtar eller ställer in råbyte för bilden som lagras i formen. |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize/) { get; } | Får information om bildstorlek och upplösning. |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype/) { get; } | Hämtar typen av bild. |
| [IsLink](../../aspose.words.drawing/imagedata/islink/) { get; } | Returnerar sant om bilden är länkad till formen (när[`SourceFullName`](./sourcefullname/) anges). |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly/) { get; } | Returnerar sant om bilden är länkad och inte lagrad i dokumentet. |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname/) { get; set; } | Hämtar eller ställer in sökvägen och namnet på källfilen för den länkade bilden. |
| [Title](../../aspose.words.drawing/imagedata/title/) { get; set; } | Definierar titeln på en bild. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Save](../../aspose.words.drawing/imagedata/save/#save)(Stream) | Sparar bilden i den angivna strömmen. |
| [Save](../../aspose.words.drawing/imagedata/save/#save_1)(string) | Sparar bilden i en fil. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage)(Image) | Ställer in bilden som formen visar. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_1)(Stream) | Ställer in bilden som formen visar. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_2)(string) | Ställer in bilden som formen visar. |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray/)() | Returnerar bildbyte för alla bilder oavsett om bilden är lagrad eller länkad. |
| [ToImage](../../aspose.words.drawing/imagedata/toimage/)() | Får bilden lagrad i formen som enImage objekt. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream/)() | Skapar och returnerar en ström som innehåller bildbytes. |

### Anmärkningar

Använd[`ImageData`](../shape/imagedata/) egenskap för att komma åt och ändra bilden i en form. Du skapar inte instanser av`ImageData` klass direkt.

En bild kan lagras i en form, länkas till extern fil eller båda (länkas och lagras i dokumentet).

Oavsett om bilden är lagrad i formen eller länkad, kan du alltid komma åt den faktiska -bilden med hjälp av[`ToByteArray`](./tobytearray/) ,[`ToStream`](./tostream/) ,[`ToImage`](./toimage/) eller[`Save`](./save/) methods. Om bilden är lagrad i formen kan du också komma åt den direkt med hjälp av[`ImageBytes`](./imagebytes/) fast egendom.

För att lagra en bild i en form använd[`SetImage`](./setimage/) metod. För att länka en bild till en form, ställ in[`SourceFullName`](./sourcefullname/) fast egendom.

### Exempel

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

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
