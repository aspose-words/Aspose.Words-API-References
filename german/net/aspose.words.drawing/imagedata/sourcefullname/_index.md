---
title: ImageData.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words für .NET
description: Entdecken Sie die ImageData SourceFullName-Eigenschaft, um verknüpfte Bildpfade und Dateinamen einfach zu verwalten und so die Effizienz Ihrer Bildverarbeitung zu verbessern.
type: docs
weight: 170
url: /de/net/aspose.words.drawing/imagedata/sourcefullname/
---
## ImageData.SourceFullName property

Ruft den Pfad und den Namen der Quelldatei für das verknüpfte Bild ab oder legt diese fest.

```csharp
public string SourceFullName { get; set; }
```

## Bemerkungen

Der Standardwert ist eine leere Zeichenfolge.

Wenn`SourceFullName` ist keine leere Zeichenfolge, das Bild ist verknüpft.

## Beispiele

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

* class [ImageData](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
