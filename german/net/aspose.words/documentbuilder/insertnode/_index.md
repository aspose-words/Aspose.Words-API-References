---
title: DocumentBuilder.InsertNode
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder methode. Fügt einen Knoten vor dem Cursor ein.
type: docs
weight: 390
url: /de/net/aspose.words/documentbuilder/insertnode/
---
## DocumentBuilder.InsertNode method

Fügt einen Knoten vor dem Cursor ein.

```csharp
public void InsertNode(Node node)
```

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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


