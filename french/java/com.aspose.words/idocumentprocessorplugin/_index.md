---
title: "IDocumentProcessorPlugin"
linktitle: "IDocumentProcessorPlugin"
second_title: "Aspose.Words pour Java"
description: "Définit une interface pour un plugin de traitement de documents externe en Java."
type: docs
weight: 761
url: /fr/java/com.aspose.words/idocumentprocessorplugin/
---
```
public interface IDocumentProcessorPlugin
```

Définit une interface pour un plugin de traitement de documents externe.
## Méthodes

| Méthode | Description |
| --- | --- |
| [append(InputStream inputStream, LoadOptions loadOptions)](#append-java.io.InputStream-com.aspose.words.LoadOptions) | Ajoute le document en le chargeant avec les options de chargement spécifiées. |
| [load(InputStream inputStream, LoadOptions loadOptions)](#load-java.io.InputStream-com.aspose.words.LoadOptions) | Charge le document en utilisant les options de chargement spécifiées. |
| [save(OutputStream outputStream, SaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions)](#setImageWatermark-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | Ajoute un filigrane d'image sur chaque page du document chargé par la méthode [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions). |
| [setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions)](#setTextWatermark-java.lang.String-com.aspose.words.TextWatermarkOptions) | Ajoute un filigrane de texte sur chaque page du document chargé par la méthode [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions). |
| [toDocument()](#toDocument) | Analyse le document chargé par la méthode [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) en un objet [Document](../../com.aspose.words/document/). |
| [toPages(FixedPageSaveOptions saveOptions)](#toPages-com.aspose.words.FixedPageSaveOptions) | Enregistre chaque page du document chargé par la méthode [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) en utilisant les options d'enregistrement de page fixe spécifiées. |
### append(InputStream inputStream, LoadOptions loadOptions) {#append-java.io.InputStream-com.aspose.words.LoadOptions}
```
public abstract void append(InputStream inputStream, LoadOptions loadOptions)
```


Ajoute le document en le chargeant avec les options de chargement spécifiées.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | Le flux d'entrée. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Les options de chargement du document. Elles peuvent être null, dans ce cas le document est chargé avec les options de chargement par défaut. |

### load(InputStream inputStream, LoadOptions loadOptions) {#load-java.io.InputStream-com.aspose.words.LoadOptions}
```
public abstract void load(InputStream inputStream, LoadOptions loadOptions)
```


Charge le document en utilisant les options de chargement spécifiées.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | Le flux d'entrée. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Les options de chargement du document. Elles peuvent être null, dans ce cas le document est chargé avec les options de chargement par défaut. |

### save(OutputStream outputStream, SaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public abstract void save(OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions) {#setImageWatermark-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public abstract void setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions)
```


Ajoute un filigrane d'image sur chaque page du document chargé par la méthode [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| imageWatermark | java.io.InputStream | Image utilisée comme filigrane. |
| imageWatermarkOptions | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Options de filigrane d'image. |

### setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions) {#setTextWatermark-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public abstract void setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions)
```


Ajoute un filigrane de texte sur chaque page du document chargé par la méthode [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions).

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| textWatermark | java.lang.String | Texte utilisé comme filigrane. |
| textWatermarkOptions | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Options de filigrane de texte. |

### toDocument() {#toDocument}
```
public abstract Document toDocument()
```


Analyse le document chargé par la méthode [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) en un objet [Document](../../com.aspose.words/document/).

**Returns:**
[Document](../../com.aspose.words/document/)
### toPages(FixedPageSaveOptions saveOptions) {#toPages-com.aspose.words.FixedPageSaveOptions}
```
public abstract OutputStream[] toPages(FixedPageSaveOptions saveOptions)
```


Enregistre chaque page du document chargé par la méthode [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) en utilisant les options d'enregistrement de page fixe spécifiées.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| saveOptions | [FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions/) |  |

**Returns:**
java.io.OutputStream[]
