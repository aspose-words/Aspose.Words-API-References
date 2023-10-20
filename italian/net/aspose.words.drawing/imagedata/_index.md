---
title: ImageData Class
linktitle: ImageData
articleTitle: ImageData
second_title: Aspose.Words per .NET
description: Aspose.Words.Drawing.ImageData classe. Definisce unimmagine per una forma in C#.
type: docs
weight: 1060
url: /it/net/aspose.words.drawing/imagedata/
---
## ImageData class

Definisce un'immagine per una forma.

Per saperne di più, visita il[Lavorare con le immagini](https://docs.aspose.com/words/net/working-with-images/) articolo di documentazione.

```csharp
public class ImageData
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel/) { get; set; } | Determina se un'immagine verrà visualizzata in bianco e nero. |
| [Borders](../../aspose.words.drawing/imagedata/borders/) { get; } | Ottiene la raccolta dei bordi dell'immagine. I bordi hanno effetto solo per le immagini in linea. |
| [Brightness](../../aspose.words.drawing/imagedata/brightness/) { get; set; } | Ottiene o imposta la luminosità dell'immagine. Il valore di questa proprietà deve essere un numero compreso tra 0,0 (più scuro) e 1,0 (più luminoso). |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey/) { get; set; } | Definisce il valore del colore dell'immagine che verrà trattata come trasparente. |
| [Contrast](../../aspose.words.drawing/imagedata/contrast/) { get; set; } | Ottiene o imposta il contrasto per l'immagine specificata. Il valore per questa proprietà deve essere un numero compreso tra 0,0 (il contrasto minimo) e 1,0 (il contrasto maggiore). |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom/) { get; set; } | Definisce la frazione di rimozione dell'immagine dal lato inferiore. |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft/) { get; set; } | Definisce la frazione di rimozione dell'immagine dal lato sinistro. |
| [CropRight](../../aspose.words.drawing/imagedata/cropright/) { get; set; } | Definisce la frazione di rimozione dell'immagine dal lato destro. |
| [CropTop](../../aspose.words.drawing/imagedata/croptop/) { get; set; } | Definisce la frazione di rimozione dell'immagine dal lato superiore. |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale/) { get; set; } | Determina se un'immagine verrà visualizzata in modalità scala di grigi. |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage/) { get; } | Restituisce`VERO` se la forma ha byte di immagine o collega un'immagine. |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes/) { get; set; } | Ottiene o imposta i byte grezzi dell'immagine archiviata nella forma. |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize/) { get; } | Ottiene informazioni sulla dimensione e sulla risoluzione dell'immagine. |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype/) { get; } | Ottiene il tipo di immagine. |
| [IsLink](../../aspose.words.drawing/imagedata/islink/) { get; } | Restituisce`VERO` se l'immagine è collegata alla forma (when[`SourceFullName`](./sourcefullname/) è specificato). |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly/) { get; } | Restituisce`VERO` se l'immagine è collegata e non memorizzata nel documento. |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname/) { get; set; } | Ottiene o imposta il percorso e il nome del file di origine per l'immagine collegata. |
| [Title](../../aspose.words.drawing/imagedata/title/) { get; set; } | Definisce il titolo di un'immagine. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Save](../../aspose.words.drawing/imagedata/save/#save)(*Stream*) | Salva l'immagine nello stream specificato. |
| [Save](../../aspose.words.drawing/imagedata/save/#save_1)(*string*) | Salva l'immagine in un file. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage)(*Image*) | Imposta l'immagine visualizzata dalla forma. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_1)(*Stream*) | Imposta l'immagine visualizzata dalla forma. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_2)(*string*) | Imposta l'immagine visualizzata dalla forma. |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray/)() | Restituisce byte immagine per qualsiasi immagine indipendentemente dal fatto che l'immagine sia archiviata o collegata. |
| [ToImage](../../aspose.words.drawing/imagedata/toimage/)() | Ottiene l'immagine memorizzata nella forma come aImage oggetto. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream/)() | Crea e restituisce uno stream che contiene i byte dell'immagine. |

## Osservazioni

Usa il[`ImageData`](../shape/imagedata/) proprietà per accedere e modificare l'immagine all'interno di una forma. Non crei istanze di`ImageData` classe direttamente.

Un'immagine può essere archiviata all'interno di una forma, collegata a un file esterno o entrambi (collegati e archiviati nel documento).

Indipendentemente dal fatto che l'immagine sia archiviata all'interno della forma o collegata, puoi sempre accedere all'immagine aware utilizzando il comando[`ToByteArray`](./tobytearray/) ,[`ToStream`](./tostream/) ,[`ToImage`](./toimage/) O[`Save`](./save/) metodi. Se l'immagine è archiviata all'interno della forma, puoi anche accedervi direttamente utilizzando il file[`ImageBytes`](./imagebytes/) proprietà.

Per memorizzare un'immagine all'interno di una forma utilizzare il comando[`SetImage`](./setimage/) metodo. Per collegare un'immagine a una forma, impostare il file[`SourceFullName`](./sourcefullname/) proprietà.

## Esempi

Mostra come estrarre immagini da un documento e salvarle nel file system locale come singoli file.

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
         // I dati immagine delle forme possono contenere immagini di molti possibili formati immagine.
        // Possiamo determinare automaticamente un'estensione di file per ciascuna immagine, in base al suo formato.
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

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
