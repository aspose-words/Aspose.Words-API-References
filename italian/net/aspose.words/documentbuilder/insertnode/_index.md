---
title: DocumentBuilder.InsertNode
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder metodo. Inserisce un nodo prima del cursore.
type: docs
weight: 390
url: /it/net/aspose.words/documentbuilder/insertnode/
---
## DocumentBuilder.InsertNode method

Inserisce un nodo prima del cursore.

```csharp
public void InsertNode(Node node)
```

### Esempi

Mostra come inserire un'immagine collegata in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Di seguito sono riportati due modi per applicare un'immagine a una forma in modo che possa visualizzarla.
// 1 - Imposta la forma per contenere l'immagine.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Ogni immagine che memorizziamo in forma aumenterà la dimensione del nostro documento.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Imposta la forma per collegarsi a un file immagine nel file system locale.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Il collegamento alle immagini farà risparmiare spazio e risulterà in un documento più piccolo.
// Tuttavia, il documento può visualizzare correttamente l'immagine solo mentre
// il file immagine è presente nella posizione a cui punta la proprietà "SourceFullName" della forma.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Guarda anche

* class [Node](../../node/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


