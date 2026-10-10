---
title: "IDocumentConverterPlugin"
linktitle: "IDocumentConverterPlugin"
second_title: "Aspose.Words per Java"
description: "Definisce un'interfaccia per un plugin convertitore esterno in Java."
type: docs
weight: 757
url: /it/java/com.aspose.words/idocumentconverterplugin/
---
```
public interface IDocumentConverterPlugin
```

Definisce un'interfaccia per un plugin convertitore esterno.
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.SaveOptions) | Converte le pagine di un documento dallo stream di input in un array di immagini. |
### convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions) {#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public abstract void convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.SaveOptions}
```
public abstract OutputStream[] convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions)
```


Converte le pagine di un documento dallo stream di input in un array di immagini.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | java.io.InputStream | Il flusso di input. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Le opzioni di caricamento del documento. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Le opzioni di salvataggio. |

**Returns:**
java.io.OutputStream[] - Array di stream di immagini delle pagine.
