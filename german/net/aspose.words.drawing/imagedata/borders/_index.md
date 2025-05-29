---
title: ImageData.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words für .NET
description: Entdecken Sie die ImageData-Border-Eigenschaft, um Inline-Bilder mit anpassbaren Rändern zu optimieren. Verbessern Sie Ihre Visualisierungen und steigern Sie noch heute die Benutzerinteraktion!
type: docs
weight: 20
url: /de/net/aspose.words.drawing/imagedata/borders/
---
## ImageData.Borders property

Ruft die Sammlung der Bildränder ab. Ränder wirken sich nur auf Inline-Bilder aus.

```csharp
public BorderCollection Borders { get; }
```

## Beispiele

Zeigt, wie die Bilddaten einer Form bearbeitet werden.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape sourceShape = (Shape)imgSourceDoc.GetChildNodes(NodeType.Shape, true)[0];

Document dstDoc = new Document();

// Importieren Sie eine Form aus dem Quelldokument und hängen Sie sie an den ersten Absatz an.
Shape importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

// Die importierte Form enthält ein Bild. Wir können über das ImageData-Objekt auf die Eigenschaften und Rohdaten des Bildes zugreifen.
ImageData imageData = importedShape.ImageData;
imageData.Title = "Imported Image";

Assert.True(imageData.HasImage);

// Wenn ein Bild keine Ränder hat, definiert sein ImageData-Objekt die Randfarbe als leer.
Assert.AreEqual(4, imageData.Borders.Count);
Assert.AreEqual(Color.Empty, imageData.Borders[0].Color);

// Dieses Bild ist nicht mit einer anderen Form oder Bilddatei im lokalen Dateisystem verknüpft.
Assert.False(imageData.IsLink);
Assert.False(imageData.IsLinkOnly);

// Die Eigenschaften „Helligkeit“ und „Kontrast“ definieren Bildhelligkeit und Kontrast
// auf einer Skala von 0 bis 1, wobei der Standardwert 0,5 ist.
imageData.Brightness = 0.8;
imageData.Contrast = 1.0;

// Die obigen Helligkeits- und Kontrastwerte haben ein Bild mit viel Weiß erzeugt.
// Wir können mit der ChromaKey-Eigenschaft eine Farbe auswählen, die durch Transparenz ersetzt werden soll, z. B. Weiß.
imageData.ChromaKey = Color.White;

// Importieren Sie die Quellform erneut und stellen Sie das Bild auf Monochrom ein.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.GrayScale = true;

// Importieren Sie die Quellform erneut, um ein drittes Bild zu erstellen und es auf BiLevel einzustellen.
// BiLevel setzt jedes Pixel entweder auf Schwarz oder Weiß, je nachdem, was der Originalfarbe näher kommt.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.BiLevel = true;

// Das Zuschneiden erfolgt auf einer Skala von 0 bis 1. Zuschneiden einer Seite um 0,3
// schneidet 30 % des Bildes auf der zugeschnittenen Seite ab.
importedShape.ImageData.CropBottom = 0.3;
importedShape.ImageData.CropLeft = 0.3;
importedShape.ImageData.CropTop = 0.3;
importedShape.ImageData.CropRight = 0.3;

dstDoc.Save(ArtifactsDir + "Drawing.ImageData.docx");
```

### Siehe auch

* class [BorderCollection](../../../aspose.words/bordercollection/)
* class [ImageData](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
