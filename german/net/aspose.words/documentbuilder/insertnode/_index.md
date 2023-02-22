---
title: DocumentBuilder.InsertNode
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder methode. Fügt einen Knoten auf Textebene innerhalb des aktuellen Absatzes vor dem Cursor ein.
type: docs
weight: 360
url: /de/net/aspose.words/documentbuilder/insertnode/
---
## DocumentBuilder.InsertNode method

Fügt einen Knoten auf Textebene innerhalb des aktuellen Absatzes vor dem Cursor ein.

```csharp
public void InsertNode(Node node)
```

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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


