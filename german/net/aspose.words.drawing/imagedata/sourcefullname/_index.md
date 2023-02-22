---
title: ImageData.SourceFullName
second_title: Aspose.Words für .NET-API-Referenz
description: ImageData eigendom. Ruft den Pfad und Namen der Quelldatei für das verknüpfte Bild ab oder legt ihn fest.
type: docs
weight: 170
url: /de/net/aspose.words.drawing/imagedata/sourcefullname/
---
## ImageData.SourceFullName property

Ruft den Pfad und Namen der Quelldatei für das verknüpfte Bild ab oder legt ihn fest.

```csharp
public string SourceFullName { get; set; }
```

### Bemerkungen

Der Standardwert ist eine leere Zeichenfolge.

Wenn`SourceFullName` kein leerer String ist, ist das Bild verlinkt.

### Beispiele

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

* class [ImageData](../)
* namensraum [Aspose.Words.Drawing](../../imagedata/)
* Montage [Aspose.Words](../../../)


