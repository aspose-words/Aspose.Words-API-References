---
title: "IDocumentConverterPlugin"
linktitle: "IDocumentConverterPlugin"
second_title: "Aspose.Words Java için"
description: "Java'da harici dönüştürücü eklentisi için bir arayüz tanımlar."
type: docs
weight: 757
url: /tr/java/com.aspose.words/idocumentconverterplugin/
---
```
public interface IDocumentConverterPlugin
```

Harici dönüştürücü eklentisi için bir arayüz tanımlar.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.SaveOptions) | Belgeden gelen akıştan sayfaları görüntü dizisine dönüştürür. |
### convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions) {#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public abstract void convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.SaveOptions}
```
public abstract OutputStream[] convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions)
```


Belgeden gelen akıştan sayfaları görüntü dizisine dönüştürür.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | java.io.InputStream | Girdi akışı. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Belge yükleme seçenekleri. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Kaydetme seçenekleri. |

**Returns:**
java.io.OutputStream[] - Sayfa görüntüsü akışlarının dizisi.
