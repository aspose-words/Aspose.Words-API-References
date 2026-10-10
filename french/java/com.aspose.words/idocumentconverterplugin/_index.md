---
title: "IDocumentConverterPlugin"
linktitle: "IDocumentConverterPlugin"
second_title: "Aspose.Words pour Java"
description: "Définit une interface pour un plugin de conversion externe en Java."
type: docs
weight: 757
url: /fr/java/com.aspose.words/idocumentconverterplugin/
---
```
public interface IDocumentConverterPlugin
```

Définit une interface pour un plugin de convertisseur externe.
## Méthodes

| Méthode | Description |
| --- | --- |
| [convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.SaveOptions) | Convertit les pages d'un document depuis le flux d'entrée en un tableau d'images. |
### convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions) {#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public abstract void convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.SaveOptions}
```
public abstract OutputStream[] convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions)
```


Convertit les pages d'un document depuis le flux d'entrée en un tableau d'images.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | Le flux d'entrée. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Les options de chargement du document. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Les options d'enregistrement. |

**Returns:**
java.io.OutputStream[] - Tableau de flux d'images de pages.
