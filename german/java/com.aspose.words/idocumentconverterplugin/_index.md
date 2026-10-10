---
title: "IDocumentConverterPlugin"
linktitle: "IDocumentConverterPlugin"
second_title: "Aspose.Words für Java"
description: "Definiert ein Interface für ein externes Konverter-Plugin in Java."
type: docs
weight: 757
url: /de/java/com.aspose.words/idocumentconverterplugin/
---
```
public interface IDocumentConverterPlugin
```

Definiert eine Schnittstelle für ein externes Konverter-Plugin.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.SaveOptions) | Konvertiert Seiten eines Dokuments aus einem Eingabestream in ein Array von Bildern. |
### convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions) {#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public abstract void convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.SaveOptions}
```
public abstract OutputStream[] convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions)
```


Konvertiert Seiten eines Dokuments aus einem Eingabestream in ein Array von Bildern.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStream | java.io.InputStream | Der Eingabestream. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Die Dokument-Ladeoptionen. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Die Speicheroptionen. |

**Returns:**
java.io.OutputStream[] - Array von Seitenbild-Streams.
