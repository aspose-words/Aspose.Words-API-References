---
title: DocumentBuilder.InsertImage
linktitle: InsertImage
articleTitle: InsertImage
second_title: Aspose.Words per .NET
description: Migliora senza sforzo i tuoi documenti con il metodo InsertImage di DocumentBuilder, che consente l'inserimento fluido di immagini .NET a grandezza naturale per effetti visivi straordinari.
type: docs
weight: 400
url: /it/net/aspose.words/documentbuilder/insertimage/
---
## InsertImage(*Image*) {#insertimage_3}

Inserisce un'immagine da un file .NETImage Oggetto nel documento. L'immagine viene inserita in linea e in scala al 100%.

```csharp
public Shape InsertImage(Image image)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| image | Image | L'immagine da inserire nel documento. |

### Valore di ritorno

Il nodo immagine appena inserito.

## Osservazioni

È possibile modificare le dimensioni dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

## Esempi

Mostra come inserire un'immagine da un oggetto in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFile = ImageDir + "Logo.jpg";

// Di seguito sono riportati tre modi per inserire un'immagine da un'istanza di un oggetto Immagine.
// 1 - Forma in linea con una dimensione predefinita basata sulle dimensioni originali dell'immagine:
builder.InsertImage(imageFile);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forma in linea con dimensioni personalizzate:
builder.InsertImage(imageFile, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forma fluttuante con dimensioni personalizzate:
builder.InsertImage(imageFile, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertImage(*string*) {#insertimage_9}

Inserisce un'immagine da un file o da un URL nel documento. L'immagine viene inserita in linea e in scala al 100%.

```csharp
public Shape InsertImage(string fileName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Il file con l'immagine. Può essere qualsiasi URI valido, locale o remoto. |

### Valore di ritorno

Il nodo immagine appena inserito.

## Osservazioni

Questo sovraccarico scaricherà automaticamente l'immagine prima di inserirla nel documento document se si specifica un URI remoto.

È possibile modificare le dimensioni dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

## Esempi

Mostra come inserire un'immagine WebP.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "WebP image.webp");

doc.Save(ArtifactsDir + "Image.InsertWebpImage.docx");
```

Mostra come inserire un'immagine gif nel documento.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Possiamo inserire un'immagine gif utilizzando un percorso o un array di byte.
// Funziona solo se DocumentBuilder è ottimizzato per Word versione 2010 o successiva.
// Nota che l'accesso ai byte dell'immagine provoca la conversione da Gif a Png.
Shape gifImage = builder.InsertImage(ImageDir + "Graphics Interchange Format.gif");

gifImage = builder.InsertImage(File.ReadAllBytes(ImageDir + "Graphics Interchange Format.gif"));

builder.Document.Save(ArtifactsDir + "InsertGif.docx");
```

Mostra come inserire una forma con un'immagine in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportate due posizioni in cui è presente il metodo "InsertShape" del generatore di documenti
// può ricavare l'immagine che verrà visualizzata dalla forma.
// 1 - Passare il nome file del file system locale di un file immagine:
builder.Write("Image from local file: ");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.Writeln();

// 2 - Passa un URL che punta a un'immagine.
builder.Write("Image from a URL: ");
builder.InsertImage(ImageUrl);
builder.Writeln();

doc.Save(ArtifactsDir + "Image.FromUrl.docx");
```

Mostra come inserire un'immagine mobile al centro di una pagina.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un'immagine mobile che apparirà dietro il testo sovrapposto e allineala al centro della pagina.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Mostra come determinare quale immagine verrà inserita.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Scalable Vector Graphics.svg");

// Aspose.Words inserisce l'immagine SVG nel documento come PNG con estensione svgBlip
// che contiene la rappresentazione dell'immagine vettoriale SVG originale.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words inserisce l'immagine SVG nel documento come PNG, proprio come fa Microsoft Word per i vecchi formati.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);

// Aspose.Words inserisce l'immagine SVG nel documento come metafile EMF per mantenere l'immagine in rappresentazione vettoriale.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Emf.docx");
```

Mostra come inserire un'immagine dal file system locale in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati tre modi per inserire un'immagine da un nome file di sistema locale.
// 1 - Forma in linea con una dimensione predefinita basata sulle dimensioni originali dell'immagine:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forma in linea con dimensioni personalizzate:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forma fluttuante con dimensioni personalizzate:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertImage(*Stream*) {#insertimage_6}

Inserisce un'immagine da un flusso nel documento. L'immagine viene inserita in linea e in scala al 100%.

```csharp
public Shape InsertImage(Stream stream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Il flusso che contiene l'immagine. |

### Valore di ritorno

Il nodo immagine appena inserito.

## Osservazioni

È possibile modificare le dimensioni dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

## Esempi

Mostra come inserire una forma con un'immagine da un flusso in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    builder.Write("Image from stream: ");
    builder.InsertImage(stream);
}

doc.Save(ArtifactsDir + "Image.FromStream.docx");
```

Mostra come inserire un'immagine da un flusso in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Di seguito sono riportati tre modi per inserire un'immagine da un flusso.
    // 1 - Forma in linea con una dimensione predefinita basata sulle dimensioni originali dell'immagine:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forma in linea con dimensioni personalizzate:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forma fluttuante con dimensioni personalizzate:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertImage(*byte[]*) {#insertimage}

Inserisce un'immagine da un array di byte nel documento. L'immagine viene inserita in linea e in scala al 100%.

```csharp
public Shape InsertImage(byte[] imageBytes)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imageBytes | Byte[] | L'array di byte che contiene l'immagine. |

### Valore di ritorno

Il nodo immagine appena inserito.

## Osservazioni

È possibile modificare le dimensioni dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

## Esempi

Mostra come inserire un'immagine da un array di byte in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageByteArray = TestUtil.ImageToByteArray(ImageDir + "Logo.jpg");

// Di seguito sono riportati tre modi per inserire un'immagine da un array di byte.
// 1 - Forma in linea con una dimensione predefinita basata sulle dimensioni originali dell'immagine:
builder.InsertImage(imageByteArray);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forma in linea con dimensioni personalizzate:
builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forma fluttuante con dimensioni personalizzate:
builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertImage(*Image, double, double*) {#insertimage_5}

Inserisce un'immagine in linea da un file .NETImage oggetto nel documento e lo ridimensiona alla dimensione specificata.

```csharp
public Shape InsertImage(Image image, double width, double height)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| image | Image | L'immagine da inserire nel documento. |
| width | Double | Larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| height | Double | Altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |

### Valore di ritorno

Il nodo immagine appena inserito.

## Osservazioni

È possibile modificare le dimensioni dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

## Esempi

Mostra come inserire un'immagine da un oggetto in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFile = ImageDir + "Logo.jpg";

// Di seguito sono riportati tre modi per inserire un'immagine da un'istanza di un oggetto Immagine.
// 1 - Forma in linea con una dimensione predefinita basata sulle dimensioni originali dell'immagine:
builder.InsertImage(imageFile);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forma in linea con dimensioni personalizzate:
builder.InsertImage(imageFile, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forma fluttuante con dimensioni personalizzate:
builder.InsertImage(imageFile, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertImage(*string, double, double*) {#insertimage_11}

Inserisce un'immagine in linea da un file o URL nel documento e la ridimensiona alla dimensione specificata.

```csharp
public Shape InsertImage(string fileName, double width, double height)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Il file che contiene l'immagine. |
| width | Double | Larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| height | Double | Altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |

### Valore di ritorno

Il nodo immagine appena inserito.

## Osservazioni

È possibile modificare le dimensioni dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

## Esempi

Mostra come inserire un'immagine dal file system locale in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati tre modi per inserire un'immagine da un nome file di sistema locale.
// 1 - Forma in linea con una dimensione predefinita basata sulle dimensioni originali dell'immagine:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forma in linea con dimensioni personalizzate:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forma fluttuante con dimensioni personalizzate:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertImage(*Stream, double, double*) {#insertimage_8}

Inserisce un'immagine in linea da un flusso nel documento e la ridimensiona alla dimensione specificata.

```csharp
public Shape InsertImage(Stream stream, double width, double height)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Il flusso che contiene l'immagine. |
| width | Double | Larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| height | Double | Altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |

### Valore di ritorno

Il nodo immagine appena inserito.

## Osservazioni

È possibile modificare le dimensioni dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

## Esempi

Mostra come inserire un'immagine da un flusso in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Di seguito sono riportati tre modi per inserire un'immagine da un flusso.
    // 1 - Forma in linea con una dimensione predefinita basata sulle dimensioni originali dell'immagine:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forma in linea con dimensioni personalizzate:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forma fluttuante con dimensioni personalizzate:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertImage(*byte[], double, double*) {#insertimage_2}

Inserisce un'immagine in linea da un array di byte nel documento e la ridimensiona alla dimensione specificata.

```csharp
public Shape InsertImage(byte[] imageBytes, double width, double height)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imageBytes | Byte[] | L'array di byte che contiene l'immagine. |
| width | Double | Larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| height | Double | Altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |

### Valore di ritorno

Il nodo immagine appena inserito.

## Osservazioni

È possibile modificare le dimensioni dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

## Esempi

Mostra come inserire un'immagine da un array di byte in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageByteArray = TestUtil.ImageToByteArray(ImageDir + "Logo.jpg");

// Di seguito sono riportati tre modi per inserire un'immagine da un array di byte.
// 1 - Forma in linea con una dimensione predefinita basata sulle dimensioni originali dell'immagine:
builder.InsertImage(imageByteArray);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forma in linea con dimensioni personalizzate:
builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forma fluttuante con dimensioni personalizzate:
builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertImage(*Image, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_4}

Inserisce un'immagine da un file .NETImage oggetto nella posizione e dimensione specificate.

```csharp
public Shape InsertImage(Image image, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| image | Image | L'immagine da inserire nel documento. |
| horzPos | RelativeHorizontalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| left | Double | Distanza in punti dall'origine al lato sinistro dell'immagine. |
| vertPos | RelativeVerticalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| top | Double | Distanza in punti dall'origine alla parte superiore dell'immagine. |
| width | Double | Larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| height | Double | Altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| wrapType | WrapType | Specifica come disporre il testo attorno all'immagine. |

### Valore di ritorno

Il nodo immagine appena inserito.

## Osservazioni

È possibile modificare le dimensioni dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

## Esempi

Mostra come inserire un'immagine da un oggetto in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFile = ImageDir + "Logo.jpg";

// Di seguito sono riportati tre modi per inserire un'immagine da un'istanza di un oggetto Immagine.
// 1 - Forma in linea con una dimensione predefinita basata sulle dimensioni originali dell'immagine:
builder.InsertImage(imageFile);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forma in linea con dimensioni personalizzate:
builder.InsertImage(imageFile, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forma fluttuante con dimensioni personalizzate:
builder.InsertImage(imageFile, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertImage(*string, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_10}

Inserisce un'immagine da un file o URL nella posizione e dimensione specificate.

```csharp
public Shape InsertImage(string fileName, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Il file che contiene l'immagine. |
| horzPos | RelativeHorizontalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| left | Double | Distanza in punti dall'origine al lato sinistro dell'immagine. |
| vertPos | RelativeVerticalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| top | Double | Distanza in punti dall'origine alla parte superiore dell'immagine. |
| width | Double | Larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| height | Double | Altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| wrapType | WrapType | Specifica come disporre il testo attorno all'immagine. |

### Valore di ritorno

Il nodo immagine appena inserito.

## Osservazioni

È possibile modificare le dimensioni dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

## Esempi

Mostra come inserire un'immagine.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Esistono due modi per utilizzare un generatore di documenti per reperire un'immagine e poi inserirla come forma mobile.
// 1 - Da un file nel file system locale:
builder.InsertImage(ImageDir + "Transparent background logo.png", RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 0, 200, 200, WrapType.Square);

// 2 - Da un URL:
builder.InsertImage(ImageUrl, RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 250, 200, 200, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFloatingImage.docx");
```

Mostra come inserire un'immagine dal file system locale in un documento mantenendone le dimensioni.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Il metodo InsertImage crea una forma mobile con l'immagine passata nei suoi dati immagine.
// Possiamo specificare le dimensioni della forma passandole a questo metodo.
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg", RelativeHorizontalPosition.Margin, 0,
    RelativeVerticalPosition.Margin, 0, -1, -1, WrapType.Square);

// Il passaggio di valori negativi come dimensioni previste definirà automaticamente
// le dimensioni della forma in base alle dimensioni della sua immagine.
Assert.AreEqual(300.0d, imageShape.Width);
Assert.AreEqual(300.0d, imageShape.Height);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertImageOriginalSize.docx");
```

Mostra come inserire un'immagine dal file system locale in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati tre modi per inserire un'immagine da un nome file di sistema locale.
// 1 - Forma in linea con una dimensione predefinita basata sulle dimensioni originali dell'immagine:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forma in linea con dimensioni personalizzate:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forma fluttuante con dimensioni personalizzate:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertImage(*Stream, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_7}

Inserisce un'immagine da un flusso nella posizione e dimensione specificate.

```csharp
public Shape InsertImage(Stream stream, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Il flusso che contiene l'immagine. |
| horzPos | RelativeHorizontalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| left | Double | Distanza in punti dall'origine al lato sinistro dell'immagine. |
| vertPos | RelativeVerticalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| top | Double | Distanza in punti dall'origine alla parte superiore dell'immagine. |
| width | Double | Larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| height | Double | Altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| wrapType | WrapType | Specifica come disporre il testo attorno all'immagine. |

### Valore di ritorno

Il nodo immagine appena inserito.

## Osservazioni

È possibile modificare le dimensioni dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

## Esempi

Mostra come inserire un'immagine da un flusso in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Di seguito sono riportati tre modi per inserire un'immagine da un flusso.
    // 1 - Forma in linea con una dimensione predefinita basata sulle dimensioni originali dell'immagine:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forma in linea con dimensioni personalizzate:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forma fluttuante con dimensioni personalizzate:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## InsertImage(*byte[], [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_1}

Inserisce un'immagine da un array di byte nella posizione e dimensione specificate.

```csharp
public Shape InsertImage(byte[] imageBytes, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imageBytes | Byte[] | L'array di byte che contiene l'immagine. |
| horzPos | RelativeHorizontalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| left | Double | Distanza in punti dall'origine al lato sinistro dell'immagine. |
| vertPos | RelativeVerticalPosition | Specifica da dove viene misurata la distanza dall'immagine. |
| top | Double | Distanza in punti dall'origine alla parte superiore dell'immagine. |
| width | Double | Larghezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| height | Double | Altezza dell'immagine in punti. Può essere un valore negativo o zero per richiedere una scala del 100%. |
| wrapType | WrapType | Specifica come disporre il testo attorno all'immagine. |

### Valore di ritorno

Il nodo immagine appena inserito.

## Osservazioni

È possibile modificare le dimensioni dell'immagine, la posizione, il metodo di posizionamento e altre impostazioni utilizzando [`Shape`](../../../aspose.words.drawing/shape/) oggetto restituito da questo metodo.

## Esempi

Mostra come inserire un'immagine da un array di byte in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageByteArray = TestUtil.ImageToByteArray(ImageDir + "Logo.jpg");

// Di seguito sono riportati tre modi per inserire un'immagine da un array di byte.
// 1 - Forma in linea con una dimensione predefinita basata sulle dimensioni originali dell'immagine:
builder.InsertImage(imageByteArray);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forma in linea con dimensioni personalizzate:
builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forma fluttuante con dimensioni personalizzate:
builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
