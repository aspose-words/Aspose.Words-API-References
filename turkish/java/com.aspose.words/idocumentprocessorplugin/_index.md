---
title: "IDocumentProcessorPlugin"
linktitle: "IDocumentProcessorPlugin"
second_title: "Aspose.Words Java için"
description: "Java'da harici belge işleyici eklentisi için bir arayüz tanımlar."
type: docs
weight: 761
url: /tr/java/com.aspose.words/idocumentprocessorplugin/
---
```
public interface IDocumentProcessorPlugin
```

Harici belge işleyici eklentisi için bir arayüz tanımlar.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [append(InputStream inputStream, LoadOptions loadOptions)](#append-java.io.InputStream-com.aspose.words.LoadOptions) | Belgeyi belirtilen yükleme seçenekleriyle yükleyerek ekleyin. |
| [load(InputStream inputStream, LoadOptions loadOptions)](#load-java.io.InputStream-com.aspose.words.LoadOptions) | Belgeyi belirtilen yükleme seçeneklerini kullanarak yükleyin. |
| [save(OutputStream outputStream, SaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions)](#setImageWatermark-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | Belgeyi [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) yöntemiyle yükleyen her sayfaya resim filigranı ekler. |
| [setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions)](#setTextWatermark-java.lang.String-com.aspose.words.TextWatermarkOptions) | Belgeyi [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) yöntemiyle yükleyen her sayfaya metin filigranı ekler. |
| [toDocument()](#toDocument) | Belgeyi [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) yöntemiyle yükleyip [Document](../../com.aspose.words/document/) nesnesine ayrıştırır. |
| [toPages(FixedPageSaveOptions saveOptions)](#toPages-com.aspose.words.FixedPageSaveOptions) | Belgeyi [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) yöntemiyle yükleyen her sayfayı belirtilen sabit sayfa kaydetme seçeneklerini kullanarak kaydeder. |
### append(InputStream inputStream, LoadOptions loadOptions) {#append-java.io.InputStream-com.aspose.words.LoadOptions}
```
public abstract void append(InputStream inputStream, LoadOptions loadOptions)
```


Belgeyi belirtilen yükleme seçenekleriyle yükleyerek ekleyin.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | java.io.InputStream | Girdi akışı. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Belge yükleme seçenekleri. null olabilir, bu durumda belge varsayılan yükleme seçenekleriyle yüklenir. |

### load(InputStream inputStream, LoadOptions loadOptions) {#load-java.io.InputStream-com.aspose.words.LoadOptions}
```
public abstract void load(InputStream inputStream, LoadOptions loadOptions)
```


Belgeyi belirtilen yükleme seçeneklerini kullanarak yükleyin.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | java.io.InputStream | Girdi akışı. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Belge yükleme seçenekleri. null olabilir, bu durumda belge varsayılan yükleme seçenekleriyle yüklenir. |

### save(OutputStream outputStream, SaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public abstract void save(OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions) {#setImageWatermark-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public abstract void setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions)
```


Belgeyi [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) yöntemiyle yükleyen her sayfaya resim filigranı ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| imageWatermark | java.io.InputStream | Filigran olarak kullanılan görüntü. |
| imageWatermarkOptions | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Görüntü filigranı seçenekleri. |

### setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions) {#setTextWatermark-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public abstract void setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions)
```


Belgeyi [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) yöntemiyle yükleyen her sayfaya metin filigranı ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textWatermark | java.lang.String | Filigran olarak kullanılan metin. |
| textWatermarkOptions | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Metin filigranı seçenekleri. |

### toDocument() {#toDocument}
```
public abstract Document toDocument()
```


Belgeyi [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) yöntemiyle yükleyip [Document](../../com.aspose.words/document/) nesnesine ayrıştırır.

**Returns:**
[Document](../../com.aspose.words/document/)
### toPages(FixedPageSaveOptions saveOptions) {#toPages-com.aspose.words.FixedPageSaveOptions}
```
public abstract OutputStream[] toPages(FixedPageSaveOptions saveOptions)
```


Belgeyi [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) yöntemiyle yükleyen her sayfayı belirtilen sabit sayfa kaydetme seçeneklerini kullanarak kaydeder.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| saveOptions | [FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions/) |  |

**Returns:**
java.io.OutputStream[]
