---
title: Watermarker.SetWatermarkToImages
linktitle: SetWatermarkToImages
articleTitle: SetWatermarkToImages
second_title: Aspose.Words per .NET
description: Migliora le tue immagini con il nostro metodo Watermarker Set, aggiungendo filigrane di testo personalizzabili per un tocco professionale e un output impeccabile.
type: docs
weight: 40
url: /it/net/aspose.words.lowcode/watermarker/setwatermarktoimages/
---
## SetWatermarkToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#setwatermarktoimages_3}

Aggiunge una filigrana di testo al documento con opzioni. Esegue il rendering dell'output in immagini.

```csharp
public static Stream[] SetWatermarkToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| saveOptions | ImageSaveOptions | Le opzioni di salvataggio. |
| watermarkText | String | Testo visualizzato come filigrana. |
| options | TextWatermarkOptions | Definisce opzioni aggiuntive per la filigrana di testo. |

## Esempi

Mostra come inserire il testo della filigrana nel documento e salvare il risultato come immagini.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Stream[] images = Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), watermarkText);

TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
images = Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), watermarkText, watermarkOptions);
```

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## SetWatermarkToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#setwatermarktoimages_1}

Aggiunge una filigrana di testo al documento con opzioni. Esegue il rendering dell'output in immagini.

```csharp
public static Stream[] SetWatermarkToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Flusso del file di input. |
| saveOptions | ImageSaveOptions | Le opzioni di salvataggio. |
| watermarkText | String | Testo visualizzato come filigrana. |
| options | TextWatermarkOptions | Definisce opzioni aggiuntive per la filigrana di testo. |

## Esempi

Mostra come inserire il testo della filigrana nel documento dal flusso e salvare il risultato come immagini.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), watermarkText);

    TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
    watermarkOptions.Color = Color.Red;
    images = Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), watermarkText, watermarkOptions);
}
```

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## SetWatermarkToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), byte[], [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setwatermarktoimages_2}

Aggiunge una filigrana immagine al documento con opzioni. Esegue il rendering dell'output in immagini.

```csharp
public static Stream[] SetWatermarkToImages(string inputFileName, ImageSaveOptions saveOptions, 
    byte[] watermarkImageBytes, ImageWatermarkOptions options = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| saveOptions | ImageSaveOptions | Le opzioni di salvataggio. |
| watermarkImageBytes | Byte[] | Byte dell'immagine visualizzati come filigrana. |
| options | ImageWatermarkOptions | Definisce opzioni aggiuntive per la filigrana dell'immagine. |

## Esempi

Mostra come inserire un'immagine di filigrana nel documento e salvare il risultato come immagini.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), File.ReadAllBytes(watermarkImage));

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), File.ReadAllBytes(watermarkImage), options);
```

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## SetWatermarkToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Stream, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setwatermarktoimages}

Aggiunge una filigrana immagine al documento con opzioni. Esegue il rendering dell'output in immagini.

```csharp
public static Stream[] SetWatermarkToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    Stream watermarkImageStream, ImageWatermarkOptions options = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Il flusso di input. |
| saveOptions | ImageSaveOptions | Le opzioni di salvataggio. |
| watermarkImageStream | Stream | Flusso di immagini visualizzato come filigrana. |
| options | ImageWatermarkOptions | Definisce opzioni aggiuntive per la filigrana dell'immagine. |

## Esempi

Mostra come inserire un'immagine di filigrana nel documento da un flusso e salvare il risultato come immagini.

```csharp
string watermarkImage = ImageDir + "Logo.jpg";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream imageStream = new FileStream(watermarkImage, FileMode.Open, FileAccess.Read))
    {
        Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), imageStream);
        Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), imageStream, new ImageWatermarkOptions() { Scale = 50 });
    }
}
```

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
