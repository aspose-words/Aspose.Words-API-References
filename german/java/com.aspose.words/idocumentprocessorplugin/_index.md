---
title: "IDocumentProcessorPlugin"
linktitle: "IDocumentProcessorPlugin"
second_title: "Aspose.Words für Java"
description: "Definiert eine Schnittstelle für ein externes Dokumentverarbeitungs‑Plugin in Java."
type: docs
weight: 761
url: /de/java/com.aspose.words/idocumentprocessorplugin/
---
```
public interface IDocumentProcessorPlugin
```

Definiert eine Schnittstelle für ein externes Dokumentverarbeitungs-Plugin.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [append(InputStream inputStream, LoadOptions loadOptions)](#append-java.io.InputStream-com.aspose.words.LoadOptions) | Fügt das Dokument hinzu, indem es mit den angegebenen Ladeoptionen geladen wird. |
| [load(InputStream inputStream, LoadOptions loadOptions)](#load-java.io.InputStream-com.aspose.words.LoadOptions) | Lade das Dokument mit den angegebenen Ladeoptionen. |
| [save(OutputStream outputStream, SaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions)](#setImageWatermark-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | Fügt jeder Seite des Dokuments, das mit der Methode [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) geladen wurde, ein Bildwasserzeichen hinzu. |
| [setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions)](#setTextWatermark-java.lang.String-com.aspose.words.TextWatermarkOptions) | Fügt jeder Seite des Dokuments, das mit der Methode [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) geladen wurde, ein Textwasserzeichen hinzu. |
| [toDocument()](#toDocument) | Parst das Dokument, das mit der Methode [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) geladen wurde, in ein [Document](../../com.aspose.words/document/) Objekt. |
| [toPages(FixedPageSaveOptions saveOptions)](#toPages-com.aspose.words.FixedPageSaveOptions) | Speichert jede Seite des Dokuments, das mit der Methode [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) geladen wurde, unter Verwendung der angegebenen festen Seiten‑Speicheroptionen. |
### append(InputStream inputStream, LoadOptions loadOptions) {#append-java.io.InputStream-com.aspose.words.LoadOptions}
```
public abstract void append(InputStream inputStream, LoadOptions loadOptions)
```


Fügt das Dokument hinzu, indem es mit den angegebenen Ladeoptionen geladen wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream | Der Eingabestream. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Die Dokument‑Ladeoptionen. Können null sein, in diesem Fall wird das Dokument mit den Standard‑Ladeoptionen geladen. |

### load(InputStream inputStream, LoadOptions loadOptions) {#load-java.io.InputStream-com.aspose.words.LoadOptions}
```
public abstract void load(InputStream inputStream, LoadOptions loadOptions)
```


Lade das Dokument mit den angegebenen Ladeoptionen.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream | Der Eingabestream. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Die Dokument‑Ladeoptionen. Können null sein, in diesem Fall wird das Dokument mit den Standard‑Ladeoptionen geladen. |

### save(OutputStream outputStream, SaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public abstract void save(OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions) {#setImageWatermark-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public abstract void setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions)
```


Fügt jeder Seite des Dokuments, das mit der Methode [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) geladen wurde, ein Bildwasserzeichen hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageWatermark | java.io.InputStream | Bild, das als Wasserzeichen verwendet wird. |
| imageWatermarkOptions | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Optionen für das Bildwasserzeichen. |

### setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions) {#setTextWatermark-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public abstract void setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions)
```


Fügt jeder Seite des Dokuments, das mit der Methode [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) geladen wurde, ein Textwasserzeichen hinzu.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| textWatermark | java.lang.String | Text, der als Wasserzeichen verwendet wird. |
| textWatermarkOptions | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Optionen für das Textwasserzeichen. |

### toDocument() {#toDocument}
```
public abstract Document toDocument()
```


Parst das Dokument, das mit der Methode [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) geladen wurde, in ein [Document](../../com.aspose.words/document/) Objekt.

**Returns:**
[Document](../../com.aspose.words/document/)
### toPages(FixedPageSaveOptions saveOptions) {#toPages-com.aspose.words.FixedPageSaveOptions}
```
public abstract OutputStream[] toPages(FixedPageSaveOptions saveOptions)
```


Speichert jede Seite des Dokuments, das mit der Methode [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) geladen wurde, unter Verwendung der angegebenen festen Seiten‑Speicheroptionen.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveOptions | [FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions/) |  |

**Returns:**
java.io.OutputStream[]
