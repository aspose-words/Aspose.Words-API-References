---
title: "IDocumentProcessorPlugin"
linktitle: "IDocumentProcessorPlugin"
second_title: "Aspose.Words para Java"
description: "Define una interfaz para complementos externos de procesador de documentos en Java."
type: docs
weight: 761
url: /es/java/com.aspose.words/idocumentprocessorplugin/
---
```
public interface IDocumentProcessorPlugin
```

Define una interfaz para un complemento de procesador de documentos externo.
## Métodos

| Método | Descripción |
| --- | --- |
| [append(InputStream inputStream, LoadOptions loadOptions)](#append-java.io.InputStream-com.aspose.words.LoadOptions) | Añade el documento cargándolo con las opciones de carga especificadas. |
| [load(InputStream inputStream, LoadOptions loadOptions)](#load-java.io.InputStream-com.aspose.words.LoadOptions) | Carga el documento usando las opciones de carga especificadas. |
| [save(OutputStream outputStream, SaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions)](#setImageWatermark-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | Añade una marca de agua de imagen en cada página del documento cargado por el método [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions). |
| [setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions)](#setTextWatermark-java.lang.String-com.aspose.words.TextWatermarkOptions) | Añade una marca de agua de texto en cada página del documento cargado por el método [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions). |
| [toDocument()](#toDocument) | Analiza el documento cargado por el método [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) en un objeto [Document](../../com.aspose.words/document/). |
| [toPages(FixedPageSaveOptions saveOptions)](#toPages-com.aspose.words.FixedPageSaveOptions) | Guarda cada página del documento cargado por el método [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) usando las opciones de guardado de página fija especificadas. |
### append(InputStream inputStream, LoadOptions loadOptions) {#append-java.io.InputStream-com.aspose.words.LoadOptions}
```
public abstract void append(InputStream inputStream, LoadOptions loadOptions)
```


Añade el documento cargándolo con las opciones de carga especificadas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream | El flujo de entrada. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Las opciones de carga del documento. Puede ser null, en cuyo caso el documento se carga con las opciones de carga predeterminadas. |

### load(InputStream inputStream, LoadOptions loadOptions) {#load-java.io.InputStream-com.aspose.words.LoadOptions}
```
public abstract void load(InputStream inputStream, LoadOptions loadOptions)
```


Carga el documento usando las opciones de carga especificadas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream | El flujo de entrada. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Las opciones de carga del documento. Puede ser null, en cuyo caso el documento se carga con las opciones de carga predeterminadas. |

### save(OutputStream outputStream, SaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public abstract void save(OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions) {#setImageWatermark-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public abstract void setImageWatermark(InputStream imageWatermark, ImageWatermarkOptions imageWatermarkOptions)
```


Añade una marca de agua de imagen en cada página del documento cargado por el método [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imageWatermark | java.io.InputStream | Imagen utilizada como marca de agua. |
| imageWatermarkOptions | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Opciones de marca de agua de imagen. |

### setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions) {#setTextWatermark-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public abstract void setTextWatermark(String textWatermark, TextWatermarkOptions textWatermarkOptions)
```


Añade una marca de agua de texto en cada página del documento cargado por el método [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| textWatermark | java.lang.String | Texto utilizado como marca de agua. |
| textWatermarkOptions | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Opciones de marca de agua de texto. |

### toDocument() {#toDocument}
```
public abstract Document toDocument()
```


Analiza el documento cargado por el método [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) en un objeto [Document](../../com.aspose.words/document/).

**Returns:**
[Document](../../com.aspose.words/document/)
### toPages(FixedPageSaveOptions saveOptions) {#toPages-com.aspose.words.FixedPageSaveOptions}
```
public abstract OutputStream[] toPages(FixedPageSaveOptions saveOptions)
```


Guarda cada página del documento cargado por el método [load(java.io.InputStream, com.aspose.words.LoadOptions)](../../com.aspose.words/idocumentprocessorplugin/\#load-java.io.InputStream--com.aspose.words.LoadOptions) usando las opciones de guardado de página fija especificadas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| saveOptions | [FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions/) |  |

**Returns:**
java.io.OutputStream[]
