---
title: ImageData
second_title: Aspose.Words für .NET-API-Referenz
description: Definiert ein Bild für eine Form.
type: docs
weight: 930
url: /de/net/aspose.words.drawing/imagedata/
---
## ImageData class

Definiert ein Bild für eine Form.

```csharp
public class ImageData
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel/) { get; set; } | Legt fest, ob ein Bild in Schwarzweiß angezeigt wird. |
| [Borders](../../aspose.words.drawing/imagedata/borders/) { get; } | Ruft die Sammlung der Ränder des Bildes ab. Rahmen wirken sich nur auf eingebettete Bilder aus. |
| [Brightness](../../aspose.words.drawing/imagedata/brightness/) { get; set; } | Ruft die Helligkeit des Bildes ab oder legt sie fest. Der Wert für diese Eigenschaft muss eine Zahl zwischen 0,0 (am dunkelsten) und 1,0 (am hellsten) sein. |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey/) { get; set; } | Definiert den Farbwert des Bildes, das als transparent behandelt wird. |
| [Contrast](../../aspose.words.drawing/imagedata/contrast/) { get; set; } | Holt oder setzt den Kontrast für das angegebene Bild. Der Wert für diese Eigenschaft muss eine Zahl zwischen 0,0 (geringster Kontrast) und 1,0 (größter Kontrast) sein. |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom/) { get; set; } | Definiert den Anteil der Bildentfernung von der Unterseite. |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft/) { get; set; } | Definiert den Anteil der Bildentfernung von der linken Seite. |
| [CropRight](../../aspose.words.drawing/imagedata/cropright/) { get; set; } | Definiert den Anteil der Bildentfernung von der rechten Seite. |
| [CropTop](../../aspose.words.drawing/imagedata/croptop/) { get; set; } | Definiert den Anteil der Bildentfernung von der oberen Seite. |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale/) { get; set; } | Legt fest, ob ein Bild im Graustufenmodus angezeigt wird. |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage/) { get; } | Gibt „true“ zurück, wenn die Form Bildbytes enthält oder ein Bild verknüpft. |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes/) { get; set; } | Ruft die Rohbytes des in der Form gespeicherten Bilds ab oder legt sie fest. |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize/) { get; } | Ruft die Informationen über Bildgröße und Auflösung ab. |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype/) { get; } | Ruft den Typ des Bildes ab. |
| [IsLink](../../aspose.words.drawing/imagedata/islink/) { get; } | Gibt true zurück, wenn das Bild mit der Form verknüpft ist (when[`SourceFullName`](./sourcefullname/) angegeben ist). |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly/) { get; } | Gibt „true“ zurück, wenn das Bild verknüpft und nicht im Dokument gespeichert ist. |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname/) { get; set; } | Ruft den Pfad und Namen der Quelldatei für das verknüpfte Bild ab oder legt ihn fest. |
| [Title](../../aspose.words.drawing/imagedata/title/) { get; set; } | Definiert den Titel eines Bildes. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Save](../../aspose.words.drawing/imagedata/save/#save)(Stream) | Speichert das Bild im angegebenen Stream. |
| [Save](../../aspose.words.drawing/imagedata/save/#save_1)(string) | Speichert das Bild in einer Datei. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage)(Image) | Legt das Bild fest, das die Form anzeigt. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_1)(Stream) | Legt das Bild fest, das die Form anzeigt. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_2)(string) | Legt das Bild fest, das die Form anzeigt. |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray/)() | Gibt Bildbytes für jedes Bild zurück, unabhängig davon, ob das Bild gespeichert oder verknüpft ist. |
| [ToImage](../../aspose.words.drawing/imagedata/toimage/)() | Ruft das in der Form gespeicherte Bild als a abImage Objekt. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream/)() | Erstellt und gibt einen Stream zurück, der die Bildbytes enthält. |

### Bemerkungen

Verwenden Sie die[`ImageData`](../shape/imagedata/) -Eigenschaft, um auf das Bild in einer Form zuzugreifen und es zu ändern. Sie erstellen keine Instanzen der[`ImageData`](./imagedata/) Klasse direkt.

Ein Bild kann in einer Form gespeichert, mit einer externen Datei verknüpft oder beides (verknüpft und im Dokument gespeichert) werden.

Unabhängig davon, ob das Bild in der Form gespeichert oder verknüpft ist, können Sie immer auf das Bild „actual “ zugreifen, indem Sie verwenden[`ToByteArray`](./tobytearray/) ,[`ToStream`](./tostream/) ,[`ToImage`](./toimage/) oder[`Save`](./save/) Methoden. Wenn das Bild innerhalb der Form gespeichert ist, können Sie auch direkt darauf zugreifen, indem Sie die verwenden[`ImageBytes`](./imagebytes/) Eigentum.

Um ein Bild in einer Form zu speichern, verwenden Sie die[`SetImage`](./setimage/) Methode. Um ein Bild mit einer Form zu verknüpfen, legen Sie fest[`SourceFullName`](./sourcefullname/) Eigentum.

### Beispiele

Zeigt, wie Bilder aus einem Dokument extrahiert und als einzelne Dateien im lokalen Dateisystem gespeichert werden.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Holen Sie sich die Sammlung von Formen aus dem Dokument,
// und die Bilddaten jeder Form mit einem Bild als Datei im lokalen Dateisystem speichern.
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

// Nachfolgend finden Sie zwei Möglichkeiten, ein Bild auf eine Form anzuwenden, damit es angezeigt werden kann.
// 1 - Stellen Sie die Form so ein, dass sie das Bild enthält.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Jedes Bild, das wir in Form speichern, erhöht die Größe unseres Dokuments.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Stellen Sie die Form so ein, dass sie mit einer Bilddatei im lokalen Dateisystem verknüpft wird.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Das Verlinken mit Bildern spart Platz und führt zu einem kleineren Dokument.
// Das Dokument kann das Bild jedoch nur solange korrekt anzeigen
// Die Bilddatei ist an der Stelle vorhanden, auf die die "SourceFullName"-Eigenschaft der Form zeigt.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
