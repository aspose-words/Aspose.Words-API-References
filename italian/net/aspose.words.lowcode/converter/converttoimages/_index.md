---
title: Converter.ConvertToImages
linktitle: ConvertToImages
articleTitle: ConvertToImages
second_title: Aspose.Words per .NET
description: Trasforma i tuoi documenti senza sforzo con ConvertToImages. Converti le pagine in file immagine di alta qualità in modo rapido e semplice, per una condivisione e un'archiviazione ottimizzate.
type: docs
weight: 30
url: /it/net/aspose.words.lowcode/converter/converttoimages/
---
## ConvertToImages(*string, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_5}

Converte le pagine del file di input specificato in immagini nel formato specificato e restituisce un array di flussi contenenti le immagini.

```csharp
public static Stream[] ConvertToImages(string inputFile, SaveFormat saveFormat)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | String | Nome del file di input. |
| saveFormat | SaveFormat | Formato di salvataggio. Sono consentiti solo formati di salvataggio immagine. |

### Valore di ritorno

Restituisce un array di flussi di immagini. I flussi devono essere eliminati dall'utente finale.

## Esempi

Mostra come convertire un documento in un flusso di immagini.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ConvertToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_6}

Converte le pagine del file di input specificato in immagini utilizzando le opzioni di salvataggio specificate e restituisce un array di flussi contenenti le immagini.

```csharp
public static Stream[] ConvertToImages(string inputFile, ImageSaveOptions saveOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | String | Nome del file di input. |
| saveOptions | ImageSaveOptions | Opzioni di salvataggio delle immagini. |

### Valore di ritorno

Restituisce un array di flussi di immagini. I flussi devono essere eliminati dall'utente finale.

## Esempi

Mostra come convertire un documento in un flusso di immagini.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_3}

Converte le pagine del flusso di input specificato in immagini nel formato specificato e restituisce un array di flussi contenenti le immagini.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, SaveFormat saveFormat)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Il flusso di input. |
| saveFormat | SaveFormat | Formato di salvataggio. Sono consentiti solo formati di salvataggio immagine. |

### Valore di ritorno

Restituisce un array di flussi di immagini. I flussi devono essere eliminati dall'utente finale.

## Esempi

Mostra come convertire un documento in immagini da un flusso.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_4}

Converte le pagine del flusso di input specificato in immagini utilizzando le opzioni di salvataggio specificate e restituisce un array di flussi contenenti le immagini.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, ImageSaveOptions saveOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Il flusso di input. |
| saveOptions | ImageSaveOptions | Opzioni di salvataggio delle immagini. |

### Valore di ritorno

Restituisce un array di flussi di immagini. I flussi devono essere eliminati dall'utente finale.

## Esempi

Mostra come convertire un documento in immagini da un flusso.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Guarda anche

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_2}

Converte le pagine del flusso di input specificato in immagini utilizzando le opzioni di caricamento e salvataggio fornite e restituisce un array di flussi contenenti le immagini.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, LoadOptions loadOptions, 
    ImageSaveOptions saveOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Il flusso di input. |
| loadOptions | LoadOptions | Opzioni di caricamento del documento di input. |
| saveOptions | ImageSaveOptions | Opzioni di salvataggio delle immagini. |

### Valore di ritorno

Restituisce un array di flussi di immagini. I flussi devono essere eliminati dall'utente finale.

## Esempi

Mostra come convertire un documento in immagini da un flusso.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Guarda anche

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ConvertToImages(*[Document](../../../aspose.words/document/), [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages}

Converte le pagine del documento specificato in immagini nel formato specificato e restituisce un array di flussi contenenti le immagini.

```csharp
public static Stream[] ConvertToImages(Document doc, SaveFormat saveFormat)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | Document | Il documento di input. |
| saveFormat | SaveFormat | Formato di salvataggio. Sono consentiti solo formati di salvataggio immagine. |

### Valore di ritorno

Restituisce un array di flussi di immagini. I flussi devono essere eliminati dall'utente finale.

## Esempi

Mostra come convertire un documento in un flusso di immagini.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Guarda anche

* class [Document](../../../aspose.words/document/)
* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## ConvertToImages(*[Document](../../../aspose.words/document/), [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_1}

Converte le pagine del documento specificato in immagini utilizzando le opzioni di salvataggio specificate e restituisce un array di flussi contenenti le immagini.

```csharp
public static Stream[] ConvertToImages(Document doc, ImageSaveOptions saveOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | Document | Il documento di input. |
| saveOptions | ImageSaveOptions | Opzioni di salvataggio delle immagini. |

### Valore di ritorno

Restituisce un array di flussi di immagini. I flussi devono essere eliminati dall'utente finale.

## Esempi

Mostra come convertire un documento in un flusso di immagini.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Guarda anche

* class [Document](../../../aspose.words/document/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
