---
title: ImageData.SetImage
second_title: Aspose.Words per .NET API Reference
description: ImageData metodo. Imposta limmagine visualizzata dalla forma.
type: docs
weight: 200
url: /it/net/aspose.words.drawing/imagedata/setimage/
---
## SetImage(Image) {#setimage}

Imposta l'immagine visualizzata dalla forma.

```csharp
public void SetImage(Image image)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| image | Image | L'oggetto immagine. |

### Esempi

Mostra come visualizzare le immagini dal file system locale in un documento.

```csharp
Document doc = new Document();

// Per visualizzare un'immagine in un documento, dovremo creare una forma
// che conterrà un'immagine, quindi la aggiungerà al corpo del documento.
Shape imgShape;

// Di seguito sono riportati due modi per ottenere un'immagine da un file nel file system locale.
// 1 - Crea un oggetto immagine da un file immagine:
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 - Apri un file immagine dal file system locale utilizzando un flusso:
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### Guarda anche

* class [ImageData](../)
* spazio dei nomi [Aspose.Words.Drawing](../../imagedata/)
* assemblea [Aspose.Words](../../../)

---

## SetImage(Stream) {#setimage_1}

Imposta l'immagine visualizzata dalla forma.

```csharp
public void SetImage(Stream stream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Il flusso che contiene l'immagine. |

### Esempi

Mostra come visualizzare le immagini dal file system locale in un documento.

```csharp
Document doc = new Document();

// Per visualizzare un'immagine in un documento, dovremo creare una forma
// che conterrà un'immagine, quindi la aggiungerà al corpo del documento.
Shape imgShape;

// Di seguito sono riportati due modi per ottenere un'immagine da un file nel file system locale.
// 1 - Crea un oggetto immagine da un file immagine:
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 - Apri un file immagine dal file system locale utilizzando un flusso:
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### Guarda anche

* class [ImageData](../)
* spazio dei nomi [Aspose.Words.Drawing](../../imagedata/)
* assemblea [Aspose.Words](../../../)

---

## SetImage(string) {#setimage_2}

Imposta l'immagine visualizzata dalla forma.

```csharp
public void SetImage(string fileName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Il file immagine. Può essere un nome file o un URL. |

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

// Ogni immagine che memorizziamo in forma aumenterà le dimensioni del nostro documento.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Imposta la forma da collegare a un file immagine nel file system locale.
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

* class [ImageData](../)
* spazio dei nomi [Aspose.Words.Drawing](../../imagedata/)
* assemblea [Aspose.Words](../../../)


