---
title: DocumentBuilder.InsertNode
linktitle: InsertNode
articleTitle: InsertNode
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Dokumenterstellung mit der InsertNode-Methode von DocumentBuilder. Fügen Sie mühelos Knoten vor dem Cursor ein und bearbeiten Sie sie nahtlos!
type: docs
weight: 410
url: /de/net/aspose.words/documentbuilder/insertnode/
---
## DocumentBuilder.InsertNode method

Fügt einen Knoten vor dem Cursor ein.

```csharp
public void InsertNode(Node node)
```

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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
