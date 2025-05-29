---
title: ImageData Class
linktitle: ImageData
articleTitle: ImageData
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.ImageData – Ihre Lösung zum Definieren und Verwalten von Bildern in Formen. Verbessern Sie Ihr Dokumentdesign mühelos!
type: docs
weight: 1390
url: /de/net/aspose.words.drawing/imagedata/
---
## ImageData class

Definiert ein Bild für eine Form.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Bildern](https://docs.aspose.com/words/net/working-with-images/) Dokumentationsartikel.

```csharp
public class ImageData
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel/) { get; set; } | Bestimmt, ob ein Bild in Schwarzweiß angezeigt wird. |
| [Borders](../../aspose.words.drawing/imagedata/borders/) { get; } | Ruft die Sammlung der Bildränder ab. Ränder wirken sich nur auf Inline-Bilder aus. |
| [Brightness](../../aspose.words.drawing/imagedata/brightness/) { get; set; } | Ruft die Helligkeit des Bildes ab oder legt sie fest. Der Wert für diese Eigenschaft muss eine Zahl zwischen 0,0 (am dunkelsten) und 1,0 (am hellsten) sein. |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey/) { get; set; } | Definiert den Farbwert des Bildes, der als transparent behandelt wird. |
| [Contrast](../../aspose.words.drawing/imagedata/contrast/) { get; set; } | Ruft den Kontrast für das angegebene Bild ab oder legt ihn fest. Der Wert für diese Eigenschaft muss eine Zahl zwischen 0,0 (geringster Kontrast) und 1,0 (größter Kontrast) sein. |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom/) { get; set; } | Definiert den Anteil der Bildentfernung von der Unterseite. |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft/) { get; set; } | Definiert den Anteil der Bildentfernung von der linken Seite. |
| [CropRight](../../aspose.words.drawing/imagedata/cropright/) { get; set; } | Definiert den Anteil der Bildentfernung von der rechten Seite. |
| [CropTop](../../aspose.words.drawing/imagedata/croptop/) { get; set; } | Definiert den Anteil der Bildentfernung von der Oberseite. |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale/) { get; set; } | Bestimmt, ob ein Bild im Graustufenmodus angezeigt wird. |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage/) { get; } | Rückgaben`WAHR` wenn die Form Bildbytes enthält oder ein Bild verlinkt. |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes/) { get; set; } | Ruft die Rohbytes des in der Form gespeicherten Bildes ab oder legt sie fest. |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize/) { get; } | Ruft Informationen zu Bildgröße und Auflösung ab. |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype/) { get; } | Ruft den Typ des Bildes ab. |
| [IsLink](../../aspose.words.drawing/imagedata/islink/) { get; } | Rückgaben`WAHR` wenn das Bild mit der Form verknüpft ist (wenn[`SourceFullName`](./sourcefullname/) angegeben ist). |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly/) { get; } | Rückgaben`WAHR` wenn das Bild verknüpft und nicht im Dokument gespeichert ist. |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname/) { get; set; } | Ruft den Pfad und den Namen der Quelldatei für das verknüpfte Bild ab oder legt diese fest. |
| [Title](../../aspose.words.drawing/imagedata/title/) { get; set; } | Definiert den Titel eines Bildes. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [FitImageToShape](../../aspose.words.drawing/imagedata/fitimagetoshape/)() | Passt die Bilddaten an den Formrahmen an, sodass das Seitenverhältnis der Bilddaten dem Seitenverhältnis des Formrahmens entspricht. |
| [Save](../../aspose.words.drawing/imagedata/save/#save)(*Stream*) | Speichert das Bild im angegebenen Stream. |
| [Save](../../aspose.words.drawing/imagedata/save/#save_1)(*string*) | Speichert das Bild in einer Datei. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage)(*Image*) | Legt das Bild fest, das die Form anzeigt. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_1)(*Stream*) | Legt das Bild fest, das die Form anzeigt. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_2)(*string*) | Legt das Bild fest, das die Form anzeigt. |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray/)() | Gibt Bildbytes für jedes Bild zurück, unabhängig davon, ob das Bild gespeichert oder verknüpft ist. |
| [ToImage](../../aspose.words.drawing/imagedata/toimage/)() | Ruft das in der Form gespeicherte Bild alsImage Objekt. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream/)() | Erstellt und gibt einen Stream zurück, der die Bildbytes enthält. |

## Bemerkungen

Verwenden Sie die[`ImageData`](../shape/imagedata/)Eigenschaft, um auf das Bild innerhalb einer Form zuzugreifen und es zu ändern. Sie erstellen keine Instanzen der`ImageData` Klasse direkt.

Ein Bild kann in einer Form gespeichert, mit einer externen Datei verknüpft oder beides (verknüpft und im Dokument gespeichert) sein.

Unabhängig davon, ob das Bild in der Form gespeichert oder verknüpft ist, können Sie immer auf das tatsächliche -Bild zugreifen, indem Sie[`ToByteArray`](./tobytearray/) ,[`ToStream`](./tostream/) ,[`ToImage`](./toimage/) oder[`Save`](./save/) methods. Wenn das Bild in der Form gespeichert ist, können Sie auch direkt darauf zugreifen, indem Sie[`ImageBytes`](./imagebytes/) Eigentum.

Um ein Bild in einer Form zu speichern, verwenden Sie die[`SetImage`](./setimage/) Methode. Um ein Bild mit einer Form zu verknüpfen, legen Sie die[`SourceFullName`](./sourcefullname/) Eigentum.

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

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
