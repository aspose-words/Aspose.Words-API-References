---
title: Class ImageData
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.ImageData klas. Definiert ein Bild für eine Form.
type: docs
weight: 1060
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
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel/) { get; set; } | Legt fest, ob ein Bild in Schwarzweiß angezeigt wird. |
| [Borders](../../aspose.words.drawing/imagedata/borders/) { get; } | Ruft die Sammlung der Ränder des Bildes ab. Ränder wirken sich nur auf Inline-Bilder aus. |
| [Brightness](../../aspose.words.drawing/imagedata/brightness/) { get; set; } | Ruft die Helligkeit des Bildes ab oder legt sie fest. Der Wert für diese Eigenschaft muss eine Zahl von 0,0 (am dunkelsten) bis 1,0 (am hellsten) sein. |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey/) { get; set; } | Definiert den Farbwert des Bildes, der als transparent behandelt wird. |
| [Contrast](../../aspose.words.drawing/imagedata/contrast/) { get; set; } | Ruft den Kontrast für das angegebene Bild ab oder legt diesen fest. Der Wert für diese Eigenschaft muss eine Zahl zwischen 0,0 (geringster Kontrast) und 1,0 (größter Kontrast) sein. |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom/) { get; set; } | Definiert den Anteil der Bildentfernung von der Unterseite. |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft/) { get; set; } | Definiert den Anteil der Bildentfernung von der linken Seite. |
| [CropRight](../../aspose.words.drawing/imagedata/cropright/) { get; set; } | Definiert den Anteil der Bildentfernung von der rechten Seite. |
| [CropTop](../../aspose.words.drawing/imagedata/croptop/) { get; set; } | Definiert den Anteil der Bildentfernung von der Oberseite. |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale/) { get; set; } | Legt fest, ob ein Bild im Graustufenmodus angezeigt wird. |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage/) { get; } | Gibt zurück`WAHR` wenn die Form Bildbytes hat oder ein Bild verknüpft. |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes/) { get; set; } | Ruft die Rohbytes des in der Form gespeicherten Bildes ab oder legt diese fest. |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize/) { get; } | Ruft Informationen zur Bildgröße und Auflösung ab. |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype/) { get; } | Ruft den Typ des Bildes ab. |
| [IsLink](../../aspose.words.drawing/imagedata/islink/) { get; } | Gibt zurück`WAHR` wenn das Bild mit der Form verknüpft ist (wann[`SourceFullName`](./sourcefullname/) angegeben ist). |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly/) { get; } | Gibt zurück`WAHR` wenn das Bild verlinkt und nicht im Dokument gespeichert ist. |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname/) { get; set; } | Ruft den Pfad und Namen der Quelldatei für das verknüpfte Bild ab oder legt diesen fest. |
| [Title](../../aspose.words.drawing/imagedata/title/) { get; set; } | Definiert den Titel eines Bildes. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [FitImageToShape](../../aspose.words.drawing/imagedata/fitimagetoshape/)() |  |
| [Save](../../aspose.words.drawing/imagedata/save/#save)(Stream) | Speichert das Bild im angegebenen Stream. |
| [Save](../../aspose.words.drawing/imagedata/save/#save_1)(string) | Speichert das Bild in einer Datei. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage)(Image) | Legt das Bild fest, das die Form anzeigt. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_1)(Stream) | Legt das Bild fest, das die Form anzeigt. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_2)(string) | Legt das Bild fest, das die Form anzeigt. |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray/)() | Gibt Bildbytes für jedes Bild zurück, unabhängig davon, ob das Bild gespeichert oder verknüpft ist. |
| [ToImage](../../aspose.words.drawing/imagedata/toimage/)() | Ruft das in der Form gespeicherte Bild als abImage Objekt. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream/)() | Erstellt einen Stream, der die Bildbytes enthält, und gibt ihn zurück. |

### Bemerkungen

Benutzen Sie die[`ImageData`](../shape/imagedata/) Eigenschaft, um auf das Bild innerhalb einer Form zuzugreifen und es zu ändern. Sie erstellen keine Instanzen davon`ImageData` Klasse direkt.

Ein Bild kann in einer Form gespeichert, mit einer externen Datei verknüpft oder beides (verknüpft und im Dokument gespeichert) werden.

Unabhängig davon, ob das Bild innerhalb der Form gespeichert oder verknüpft ist, können Sie jederzeit über das auf das tatsächliche -Bild zugreifen[`ToByteArray`](./tobytearray/) ,[`ToStream`](./tostream/) ,[`ToImage`](./toimage/) oder[`Save`](./save/) methoden. Wenn das Bild in der Form gespeichert ist, können Sie auch direkt über die darauf zugreifen[`ImageBytes`](./imagebytes/) Eigentum.

Um ein Bild in einer Form zu speichern, verwenden Sie die[`SetImage`](./setimage/) Methode. Um ein Bild mit einer Form zu verknüpfen, legen Sie fest[`SourceFullName`](./sourcefullname/) Eigentum.

### Beispiele

Zeigt, wie man Bilder aus einem Dokument extrahiert und sie als einzelne Dateien im lokalen Dateisystem speichert.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Holen Sie sich die Formensammlung aus dem Dokument,
// und die Bilddaten jeder Form mit einem Bild als Datei im lokalen Dateisystem speichern.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Die Bilddaten von Formen können Bilder in vielen möglichen Bildformaten enthalten.
        // Wir können für jedes Bild automatisch eine Dateierweiterung anhand seines Formats ermitteln.
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

// Im Folgenden finden Sie zwei Möglichkeiten, ein Bild auf eine Form anzuwenden, damit diese angezeigt werden kann.
// 1 – Legen Sie die Form so fest, dass sie das Bild enthält.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Jedes Bild, das wir in Form speichern, vergrößert unser Dokument.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 – Legen Sie die Form so fest, dass sie mit einer Bilddatei im lokalen Dateisystem verknüpft wird.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Das Verlinken mit Bildern spart Platz und führt zu einem kleineren Dokument.
// Allerdings kann das Dokument das Bild nur dann korrekt anzeigen, wenn
// Die Bilddatei ist an der Stelle vorhanden, auf die die „SourceFullName“-Eigenschaft der Form verweist.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)


