---
title: "IDocumentConverterPlugin"
linktitle: "IDocumentConverterPlugin"
second_title: "Aspose.Words para Java"
description: "Define una interfaz para un complemento conversor externo en Java."
type: docs
weight: 757
url: /es/java/com.aspose.words/idocumentconverterplugin/
---
```
public interface IDocumentConverterPlugin
```

Define una interfaz para un complemento de conversor externo.
## Métodos

| Método | Descripción |
| --- | --- |
| [convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.SaveOptions) | Convierte páginas de un documento desde el flujo de entrada a una matriz de imágenes. |
### convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions) {#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public abstract void convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.SaveOptions}
```
public abstract OutputStream[] convertToImages(InputStream inputStream, LoadOptions loadOptions, SaveOptions saveOptions)
```


Convierte páginas de un documento desde el flujo de entrada a una matriz de imágenes.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream | El flujo de entrada. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Las opciones de carga del documento. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Las opciones de guardado. |

**Returns:**
java.io.OutputStream[] - Matriz de flujos de imágenes de página.
