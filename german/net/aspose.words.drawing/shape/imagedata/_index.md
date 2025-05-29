---
title: Shape.ImageData
linktitle: ImageData
articleTitle: ImageData
second_title: Aspose.Words für .NET
description: Greifen Sie mühelos auf Formbilder zu und verwalten Sie sie mit der Shape ImageData-Eigenschaft. Erhalten Sie sofort Ergebnisse oder Null, falls nicht zutreffend. Verbessern Sie Ihren Design-Workflow!
type: docs
weight: 120
url: /de/net/aspose.words.drawing/shape/imagedata/
---
## Shape.ImageData property

Bietet Zugriff auf das Bild der Form. Gibt zurück`null` wenn die Form kein Bild enthalten kann.

```csharp
public ImageData ImageData { get; }
```

## Beispiele

Zeigt, wie Bilder aus einem Dokument extrahiert und als einzelne Dateien im lokalen Dateisystem gespeichert werden.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Holen Sie sich die Sammlung von Formen aus dem Dokument,
// und speichere die Bilddaten jeder Form mit einem Bild als Datei im lokalen Dateisystem.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
            // Die Bilddaten von Formen können Bilder in vielen möglichen Bildformaten enthalten.
        // Wir können für jedes Bild automatisch eine Dateierweiterung basierend auf seinem Format bestimmen.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Zeigt, wie ein verknüpftes Bild in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Unten sind zwei Möglichkeiten aufgeführt, ein Bild auf eine Form anzuwenden, damit es angezeigt werden kann.
// 1 – Legen Sie die Form fest, die das Bild enthalten soll.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Jedes Bild, das wir in der Form speichern, vergrößert die Größe unseres Dokuments.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 – Legen Sie fest, dass die Form mit einer Bilddatei im lokalen Dateisystem verknüpft werden soll.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Durch das Verknüpfen mit Bildern wird Platz gespart und das Dokument wird kleiner.
// Allerdings kann das Dokument das Bild nur dann korrekt anzeigen, wenn
// Die Bilddatei befindet sich an dem Speicherort, auf den die Eigenschaft „SourceFullName“ der Form verweist.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Siehe auch

* class [ImageData](../../imagedata/)
* class [Shape](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
