---
title: Watermark.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words per .NET
description: Migliora i tuoi documenti con il metodo Watermark SetImage. Aggiungi senza sforzo splendide filigrane alle immagini per un tocco professionale.
type: docs
weight: 30
url: /it/net/aspose.words/watermark/setimage/
---
## SetImage(*Image*) {#setimage}

Aggiunge la filigrana dell'immagine nel documento.

```csharp
public void SetImage(Image image)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| image | Image | Immagine visualizzata come filigrana. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentNullException | Generato quando l'immagine è`null` . |

## Esempi

Mostra come creare una filigrana da un'immagine nel file system locale.

```csharp
Document doc = new Document();

            // Modifica l'aspetto della filigrana dell'immagine con un oggetto ImageWatermarkOptions,
            // quindi passarlo durante la creazione di una filigrana da un file immagine.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Abbiamo diverse opzioni per inserire l'immagine:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Guarda anche

* class [Watermark](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## SetImage(*Image, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_1}

Aggiunge la filigrana dell'immagine nel documento.

```csharp
public void SetImage(Image image, ImageWatermarkOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| image | Image | Immagine visualizzata come filigrana. |
| options | ImageWatermarkOptions | Definisce opzioni aggiuntive per la filigrana dell'immagine. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentNullException | Generato quando l'immagine è`null` . |

## Osservazioni

Se[`ImageWatermarkOptions`](../../imagewatermarkoptions/) È`null`, la filigrana verrà impostata con le opzioni predefinite.

## Esempi

Mostra come creare una filigrana da un'immagine nel file system locale.

```csharp
Document doc = new Document();

            // Modifica l'aspetto della filigrana dell'immagine con un oggetto ImageWatermarkOptions,
            // quindi passarlo durante la creazione di una filigrana da un file immagine.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Abbiamo diverse opzioni per inserire l'immagine:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Guarda anche

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## SetImage(*string, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_3}

Aggiunge la filigrana dell'immagine nel documento.

```csharp
public void SetImage(string imagePath, ImageWatermarkOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imagePath | String | Percorso al file immagine visualizzato come filigrana. |
| options | ImageWatermarkOptions | Definisce opzioni aggiuntive per la filigrana dell'immagine. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentNullException | Genera un'eccezione quando il percorso è`null` . |

## Osservazioni

Se[`ImageWatermarkOptions`](../../imagewatermarkoptions/) È`null`, la filigrana verrà impostata con le opzioni predefinite.

## Esempi

Mostra come creare una filigrana da un'immagine nel file system locale.

```csharp
Document doc = new Document();

            // Modifica l'aspetto della filigrana dell'immagine con un oggetto ImageWatermarkOptions,
            // quindi passarlo durante la creazione di una filigrana da un file immagine.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Abbiamo diverse opzioni per inserire l'immagine:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Guarda anche

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## SetImage(*Stream, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_2}

Aggiunge la filigrana dell'immagine nel documento.

```csharp
public void SetImage(Stream imageStream, ImageWatermarkOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imageStream | Stream | Il flusso contenente i dati dell'immagine visualizzati come filigrana. |
| options | ImageWatermarkOptions | Definisce opzioni aggiuntive per la filigrana dell'immagine. |

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentNullException | Genera un'eccezione quando il percorso è`null` . |

## Osservazioni

Se[`ImageWatermarkOptions`](../../imagewatermarkoptions/) È`null`, la filigrana verrà impostata con le opzioni predefinite.

## Esempi

Mostra come creare una filigrana da un flusso di immagini.

```csharp
Document doc = new Document();

// Modifica l'aspetto della filigrana dell'immagine con un oggetto ImageWatermarkOptions,
// quindi passarlo durante la creazione di una filigrana da un file immagine.
ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
imageWatermarkOptions.Scale = 5;

using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
    doc.Watermark.SetImage(imageStream, imageWatermarkOptions);

doc.Save(ArtifactsDir + "Document.ImageWatermarkStream.docx");
```

### Guarda anche

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
