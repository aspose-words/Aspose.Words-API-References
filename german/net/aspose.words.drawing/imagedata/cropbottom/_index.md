---
title: ImageData.CropBottom
second_title: Aspose.Words für .NET-API-Referenz
description: ImageData eigendom. Definiert den Anteil der Bildentfernung von der Unterseite.
type: docs
weight: 60
url: /de/net/aspose.words.drawing/imagedata/cropbottom/
---
## ImageData.CropBottom property

Definiert den Anteil der Bildentfernung von der Unterseite.

```csharp
public double CropBottom { get; set; }
```

### Bemerkungen

Der Zuschneidegrad kann zwischen -1,0 und 1,0 liegen. Der Standardwert ist 0. Beachten Sie, dass bei einem Wert von 1 überhaupt kein Bild angezeigt wird. Negative Werte führen dazu, dass das Bild von der zugeschnittenen Kante nach innen gequetscht wird (der leere Raum zwischen dem Bild und der zugeschnittenen Kante wird durch die Füllfarbe der -Form gefüllt). Positive Werte kleiner als 1 führen dazu, dass das verbleibende Bild um gestreckt wird, um es an die Form anzupassen.

Der Standardwert ist 0.

### Beispiele

Zeigt, wie die Bilddaten einer Form bearbeitet werden.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape sourceShape = (Shape)imgSourceDoc.GetChildNodes(NodeType.Shape, true)[0];

Document dstDoc = new Document();

// Eine Form aus dem Quelldokument importieren und an den ersten Absatz anhängen.
Shape importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

// Die importierte Form enthält ein Bild. Über das ImageData-Objekt können wir auf die Eigenschaften und Rohdaten des Bildes zugreifen.
ImageData imageData = importedShape.ImageData;
imageData.Title = "Imported Image";

Assert.True(imageData.HasImage);

// Wenn ein Bild keine Ränder hat, definiert sein ImageData-Objekt die Rahmenfarbe als leer.
Assert.AreEqual(4, imageData.Borders.Count);
Assert.AreEqual(Color.Empty, imageData.Borders[0].Color);

// Dieses Bild ist nicht mit einer anderen Form- oder Bilddatei im lokalen Dateisystem verknüpft.
Assert.False(imageData.IsLink);
Assert.False(imageData.IsLinkOnly);

// Die Eigenschaften „Brightness“ und „Contrast“ definieren Bildhelligkeit und Kontrast
// auf einer Skala von 0 bis 1, mit dem Standardwert 0,5.
imageData.Brightness = 0.8;
imageData.Contrast = 1.0;

// Die oben genannten Helligkeits- und Kontrastwerte haben ein Bild mit viel Weiß erzeugt.
// Wir können mit der ChromaKey-Eigenschaft eine Farbe auswählen, die durch Transparenz ersetzt werden soll, z. B. Weiß.
imageData.ChromaKey = Color.White;

// Importieren Sie die Quellform erneut und stellen Sie das Bild auf Monochrom ein.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.GrayScale = true;

// Importiere die Quellform erneut, um ein drittes Bild zu erstellen und setze es auf BiLevel.
// BiLevel setzt jedes Pixel entweder auf Schwarz oder Weiß, je nachdem, was näher an der Originalfarbe liegt.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.BiLevel = true;

// Der Zuschnitt wird auf einer Skala von 0-1 bestimmt. Beschneiden einer Seite um 0,3
// schneidet 30 % des Bildes an der beschnittenen Seite aus.
importedShape.ImageData.CropBottom = 0.3;
importedShape.ImageData.CropLeft = 0.3;
importedShape.ImageData.CropTop = 0.3;
importedShape.ImageData.CropRight = 0.3;

dstDoc.Save(ArtifactsDir + "Drawing.ImageData.docx");
```

### Siehe auch

* class [ImageData](../)
* namensraum [Aspose.Words.Drawing](../../imagedata/)
* Montage [Aspose.Words](../../../)


