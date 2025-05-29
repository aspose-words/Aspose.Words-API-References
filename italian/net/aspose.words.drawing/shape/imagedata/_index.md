---
title: Shape.ImageData
linktitle: ImageData
articleTitle: ImageData
second_title: Aspose.Words per .NET
description: Accedi e gestisci le immagini delle forme senza sforzo con la proprietà Shape ImageData. Ottieni risultati immediati o null se non applicabile. Migliora il tuo flusso di lavoro di progettazione!
type: docs
weight: 120
url: /it/net/aspose.words.drawing/shape/imagedata/
---
## Shape.ImageData property

Fornisce l'accesso all'immagine della forma. Restituisce`null` se la forma non può avere un'immagine.

```csharp
public ImageData ImageData { get; }
```

## Esempi

Mostra come estrarre immagini da un documento e salvarle nel file system locale come file singoli.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Ottieni la raccolta di forme dal documento,
// e salva i dati dell'immagine di ogni forma con un'immagine come file nel file system locale.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // I dati immagine delle forme possono contenere immagini di molti possibili formati.
        // Possiamo determinare automaticamente un'estensione di file per ogni immagine, in base al suo formato.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Mostra come inserire un'immagine collegata in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Di seguito sono riportati due modi per applicare un'immagine a una forma in modo da poterla visualizzare.
// 1 - Imposta la forma che conterrà l'immagine.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Ogni immagine che memorizziamo in un formato aumenterà la dimensione del nostro documento.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Imposta la forma per collegarla a un file immagine nel file system locale.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Il collegamento alle immagini consente di risparmiare spazio e di ottenere un documento più piccolo.
// Tuttavia, il documento può visualizzare correttamente l'immagine solo mentre
// il file immagine è presente nella posizione a cui punta la proprietà "SourceFullName" della forma.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Guarda anche

* class [ImageData](../../imagedata/)
* class [Shape](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
