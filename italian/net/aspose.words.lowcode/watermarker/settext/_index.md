---
title: Watermarker.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words per .NET
description: Migliora i tuoi documenti con il nostro metodo Watermarker SetText. Aggiungi facilmente filigrane di testo personalizzabili per migliorare il tuo branding e la tua professionalità.
type: docs
weight: 30
url: /it/net/aspose.words.lowcode/watermarker/settext/
---
## SetText(*string, string, string*) {#settext_4}

Aggiunge una filigrana di testo al documento.

```csharp
public static void SetText(string inputFileName, string outputFileName, string watermarkText)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| watermarkText | String | Testo visualizzato come filigrana. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

## Esempi

Mostra come inserire il testo della filigrana nel documento.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### Guarda anche

* class [Watermarker](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## SetText(*string, string, string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_5}

Aggiunge una filigrana di testo nel documento con opzioni.

```csharp
public static void SetText(string inputFileName, string outputFileName, string watermarkText, 
    TextWatermarkOptions options)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| watermarkText | String | Testo visualizzato come filigrana. |
| options | TextWatermarkOptions | Definisce opzioni aggiuntive per la filigrana di testo. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

## Esempi

Mostra come inserire il testo della filigrana nel documento.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### Guarda anche

* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## SetText(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_2}

Aggiunge una filigrana di testo al documento con opzioni e formato di salvataggio specificato.

```csharp
public static void SetText(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| saveFormat | SaveFormat | Formato di salvataggio. |
| watermarkText | String | Testo visualizzato come filigrana. |
| options | TextWatermarkOptions | Definisce opzioni aggiuntive per la filigrana di testo. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

## Esempi

Mostra come inserire il testo della filigrana nel documento.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## SetText(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_3}

Aggiunge una filigrana di testo al documento con opzioni e formato di salvataggio specificato.

```csharp
public static void SetText(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFileName | String | Nome del file di input. |
| outputFileName | String | Nome del file di output. |
| saveOptions | SaveOptions | Le opzioni di salvataggio. |
| watermarkText | String | Testo visualizzato come filigrana. |
| options | TextWatermarkOptions | Definisce opzioni aggiuntive per la filigrana di testo. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome del file di output specificato verrà utilizzato per generare i nomi file per ogni parte, seguendo la regola: outputFile_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un singolo file TIFF multi-frame.

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## SetText(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext}

Aggiunge una filigrana di testo nel documento dai flussi con opzioni.

```csharp
public static void SetText(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Il flusso di input. |
| outputStream | Stream | Il flusso di output. |
| saveFormat | SaveFormat | Formato di salvataggio. |
| watermarkText | String | Testo visualizzato come filigrana. |
| options | TextWatermarkOptions | Definisce opzioni aggiuntive per la filigrana di testo. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nel flusso specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nel flusso specificato.

## Esempi

Mostra come inserire il testo della filigrana nel documento dal flusso.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkTextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.SetText(streamIn, streamOut, SaveFormat.Docx, watermarkText);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkTextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
    {
        TextWatermarkOptions options = new TextWatermarkOptions();
        options.Color = Color.Red;
        Watermarker.SetText(streamIn, streamOut, SaveFormat.Docx, watermarkText, options);
    }
}
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## SetText(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_1}

Aggiunge una filigrana di testo nel documento dai flussi con opzioni.

```csharp
public static void SetText(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | Stream | Il flusso di input. |
| outputStream | Stream | Il flusso di output. |
| saveOptions | SaveOptions | Le opzioni di salvataggio. |
| watermarkText | String | Testo visualizzato come filigrana. |
| options | TextWatermarkOptions | Definisce opzioni aggiuntive per la filigrana di testo. |

## Osservazioni

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la prima pagina dell'output verrà salvata nel flusso specificato.

Se il formato di output è TIFF, l'output verrà salvato come un singolo TIFF multi-frame nel flusso specificato.

### Guarda anche

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
