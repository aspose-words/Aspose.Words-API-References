---
title: ImageData.SourceFullName
second_title: Aspose.Words für .NET-API-Referenz
description: ImageData eigendom. Ruft den Pfad und Namen der Quelldatei für das verknüpfte Bild ab oder legt diesen fest.
type: docs
weight: 170
url: /de/net/aspose.words.drawing/imagedata/sourcefullname/
---
## ImageData.SourceFullName property

Ruft den Pfad und Namen der Quelldatei für das verknüpfte Bild ab oder legt diesen fest.

```csharp
public string SourceFullName { get; set; }
```

### Bemerkungen

Der Standardwert ist eine leere Zeichenfolge.

Wenn`SourceFullName` ist kein leerer String, das Bild ist verlinkt.

### Beispiele

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

* class [ImageData](../)
* namensraum [Aspose.Words.Drawing](../../imagedata/)
* Montage [Aspose.Words](../../../)


