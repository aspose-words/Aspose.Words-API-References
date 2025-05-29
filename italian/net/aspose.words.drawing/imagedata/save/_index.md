---
title: ImageData.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words per .NET
description: Salva le immagini senza sforzo con il metodo ImageData Save. Semplifica il tuo flusso di lavoro memorizzando le immagini direttamente nel flusso che preferisci con facilità.
type: docs
weight: 200
url: /it/net/aspose.words.drawing/imagedata/save/
---
## Save(*Stream*) {#save}

Salva l'immagine nel flusso specificato.

```csharp
public void Save(Stream stream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Il flusso in cui salvare l'immagine. |

## Osservazioni

È responsabilità del chiamante eliminare l'oggetto stream.

## Esempi

Mostra come salvare tutte le immagini da un documento al file system.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// Le forme con il flag "HasImage" impostato memorizzano e visualizzano tutte le immagini del documento.
Shape[] shapesWithImages = imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>()
    .Where(s => s.HasImage).ToArray();

// Esamina ogni forma e salva la relativa immagine.
for (int shapeIndex = 0; shapeIndex < shapesWithImages.Length; ++shapeIndex)
{
    ImageData imageData = shapesWithImages[shapeIndex].ImageData;
    using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{shapeIndex + 1}.{imageData.ImageType}"))
        imageData.Save(fileStream);
}
```

### Guarda anche

* class [ImageData](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)

---

## Save(*string*) {#save_1}

Salva l'immagine in un file.

```csharp
public void Save(string fileName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Il nome del file in cui salvare l'immagine. |

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

### Guarda anche

* class [ImageData](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
