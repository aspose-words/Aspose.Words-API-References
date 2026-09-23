---
title: "IDocumentProcessorPlugin"
linktitle: "IDocumentProcessorPlugin"
second_title: "Aspose.Words для Java"
description: "Определяет интерфейс для внешнего плагина процессора документов в Java."
type: docs
weight: 761
url: /ru/java/com.aspose.words/idocumentprocessorplugin/
---
```
public interface IDocumentProcessorPlugin
```

Определяет интерфейс для внешнего плагина обработки документов.
## Методы

| Метод | Описание |
| --- | --- |
| [append(InputStream inputStream, LoadOptions loadOptions)](#append-java.io.InputStream-com.aspose.words.LoadOptions) | Добавьте документ, загрузив его с указанными параметрами загрузки. |
| [load(InputStream inputStream, LoadOptions loadOptions)](#load-java.io.InputStream-com.aspose.words.LoadOptions) | Загрузите документ, используя указанные параметры загрузки. |
| [save(OutputStream outputStream, SaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions)](#setImageWatermark-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | Добавляет изображение‑водяной знак на каждую страницу документа, загруженного методом [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions). |
| [setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions)](#setTextWatermark-java.lang.String-com.aspose.words.TextWatermarkOptions) | Добавляет текстовый водяной знак на каждую страницу документа, загруженного методом [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions). |
| [toDocument()](#toDocument) | Разбирает документ, загруженный методом [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) в объект [Document](../../com.aspose.words/document/). |
| [toPages(FixedPageSaveOptions saveOptions)](#toPages-com.aspose.words.FixedPageSaveOptions) | Сохраняет каждую страницу документа, загруженного методом [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) с использованием указанных фиксированных параметров сохранения страницы. |
### append(InputStream inputStream, LoadOptions loadOptions) {#append-java.io.InputStream-com.aspose.words.LoadOptions}
```
public abstract void append(InputStream inputStream, LoadOptions loadOptions)
```


Добавьте документ, загрузив его с указанными параметрами загрузки.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream | Входной поток. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Параметры загрузки документа. Может быть null, в этом случае документ загружается с параметрами загрузки по умолчанию. |

### load(InputStream inputStream, LoadOptions loadOptions) {#load-java.io.InputStream-com.aspose.words.LoadOptions}
```
public abstract void load(InputStream inputStream, LoadOptions loadOptions)
```


Загрузите документ, используя указанные параметры загрузки.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream | Входной поток. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Параметры загрузки документа. Может быть null, в этом случае документ загружается с параметрами загрузки по умолчанию. |

### save(OutputStream outputStream, SaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public abstract void save(OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions) {#setImageWatermark-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public abstract void setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions)
```


Добавляет изображение‑водяной знак на каждую страницу документа, загруженного методом [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| imageWatermark | java.io.InputStream | Изображение, используемое в качестве водяного знака. |
| imageWatermarkOptions | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Параметры водяного знака изображения. |

### setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions) {#setTextWatermark-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public abstract void setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions)
```


Добавляет текстовый водяной знак на каждую страницу документа, загруженного методом [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| textWatermark | java.lang.String | Текст, используемый в качестве водяного знака. |
| textWatermarkOptions | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Параметры текстового водяного знака. |

### toDocument() {#toDocument}
```
public abstract Document toDocument()
```


Разбирает документ, загруженный методом [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) в объект [Document](../../com.aspose.words/document/).

**Returns:**
[Document](../../com.aspose.words/document/)
### toPages(FixedPageSaveOptions saveOptions) {#toPages-com.aspose.words.FixedPageSaveOptions}
```
public abstract OutputStream[] toPages(FixedPageSaveOptions saveOptions)
```


Сохраняет каждую страницу документа, загруженного методом [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) с использованием указанных фиксированных параметров сохранения страницы.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| saveOptions | [FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions/) |  |

**Returns:**
java.io.OutputStream[]
