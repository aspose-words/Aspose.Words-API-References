---
title: "IDocumentProcessorPlugin"
linktitle: "IDocumentProcessorPlugin"
second_title: "Aspose.Words per Java"
description: "Definisce un'interfaccia per plugin di elaborazione documenti esterno in Java."
type: docs
weight: 761
url: /it/java/com.aspose.words/idocumentprocessorplugin/
---
```
public interface IDocumentProcessorPlugin
```

Definisce un'interfaccia per un plugin di elaborazione documenti esterno.
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [append(InputStream inputStream, LoadOptions loadOptions)](#append-java.io.InputStream-com.aspose.words.LoadOptions) | Aggiunge il documento caricandolo con le opzioni di caricamento specificate. |
| [load(InputStream inputStream, LoadOptions loadOptions)](#load-java.io.InputStream-com.aspose.words.LoadOptions) | Carica il documento utilizzando le opzioni di caricamento specificate. |
| [save(OutputStream outputStream, SaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions)](#setImageWatermark-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | Aggiunge una filigrana immagine su ogni pagina del documento caricato dal metodo [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) metodo. |
| [setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions)](#setTextWatermark-java.lang.String-com.aspose.words.TextWatermarkOptions) | Aggiunge una filigrana testo su ogni pagina del documento caricato dal metodo [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) metodo. |
| [toDocument()](#toDocument) | Analizza il documento caricato dal metodo [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) in un oggetto [Document](../../com.aspose.words/document/). |
| [toPages(FixedPageSaveOptions saveOptions)](#toPages-com.aspose.words.FixedPageSaveOptions) | Salva ogni pagina del documento caricato dal metodo [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) utilizzando le opzioni di salvataggio pagina fissa specificate. |
### append(InputStream inputStream, LoadOptions loadOptions) {#append-java.io.InputStream-com.aspose.words.LoadOptions}
```
public abstract void append(InputStream inputStream, LoadOptions loadOptions)
```


Aggiunge il documento caricandolo con le opzioni di caricamento specificate.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | java.io.InputStream | Il flusso di input. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Le opzioni di caricamento del documento. Possono essere null, in tal caso il documento viene caricato con le opzioni di caricamento predefinite. |

### load(InputStream inputStream, LoadOptions loadOptions) {#load-java.io.InputStream-com.aspose.words.LoadOptions}
```
public abstract void load(InputStream inputStream, LoadOptions loadOptions)
```


Carica il documento utilizzando le opzioni di caricamento specificate.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | java.io.InputStream | Il flusso di input. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Le opzioni di caricamento del documento. Possono essere null, in tal caso il documento viene caricato con le opzioni di caricamento predefinite. |

### save(OutputStream outputStream, SaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public abstract void save(OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions) {#setImageWatermark-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public abstract void setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions)
```


Aggiunge una filigrana immagine su ogni pagina del documento caricato dal metodo [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) metodo.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imageWatermark | java.io.InputStream | Immagine usata come filigrana. |
| imageWatermarkOptions | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Opzioni della filigrana immagine. |

### setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions) {#setTextWatermark-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public abstract void setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions)
```


Aggiunge una filigrana testo su ogni pagina del documento caricato dal metodo [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) metodo.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| textWatermark | java.lang.String | Testo usato come filigrana. |
| textWatermarkOptions | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Opzioni della filigrana testo. |

### toDocument() {#toDocument}
```
public abstract Document toDocument()
```


Analizza il documento caricato dal metodo [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) in un oggetto [Document](../../com.aspose.words/document/).

**Returns:**
[Document](../../com.aspose.words/document/)
### toPages(FixedPageSaveOptions saveOptions) {#toPages-com.aspose.words.FixedPageSaveOptions}
```
public abstract OutputStream[] toPages(FixedPageSaveOptions saveOptions)
```


Salva ogni pagina del documento caricato dal metodo [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) utilizzando le opzioni di salvataggio pagina fissa specificate.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| saveOptions | [FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions/) |  |

**Returns:**
java.io.OutputStream[]
