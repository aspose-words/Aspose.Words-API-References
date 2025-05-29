---
title: ImageData.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words för .NET
description: Spara bilder enkelt med ImageData Save-metoden. Effektivisera ditt arbetsflöde genom att enkelt lagra bilder direkt i din valda ström.
type: docs
weight: 200
url: /sv/net/aspose.words.drawing/imagedata/save/
---
## Save(*Stream*) {#save}

Sparar bilden i den angivna strömmen.

```csharp
public void Save(Stream stream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Strömmen där bilden ska sparas. |

## Anmärkningar

Är det anroparens ansvar att kassera strömobjektet.

## Exempel

Visar hur man sparar alla bilder från ett dokument till filsystemet.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// Former med flaggan "HasImage" lagrar och visar alla dokumentets bilder.
Shape[] shapesWithImages = imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>()
    .Where(s => s.HasImage).ToArray();

// Gå igenom varje form och spara dess bild.
for (int shapeIndex = 0; shapeIndex < shapesWithImages.Length; ++shapeIndex)
{
    ImageData imageData = shapesWithImages[shapeIndex].ImageData;
    using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{shapeIndex + 1}.{imageData.ImageType}"))
        imageData.Save(fileStream);
}
```

### Se även

* class [ImageData](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)

---

## Save(*string*) {#save_1}

Sparar bilden i en fil.

```csharp
public void Save(string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Filnamnet där bilden ska sparas. |

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
         // Bilddata för former kan innehålla bilder i många möjliga bildformat.
        // Vi kan automatiskt bestämma filändelsen för varje bild, baserat på dess format.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### Se även

* class [ImageData](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
