---
title: Converter.ConvertToImages
linktitle: ConvertToImages
articleTitle: ConvertToImages
second_title: Aspose.Words para .NET
description: Transforme sus documentos fácilmente con ConvertToImages. Convierta páginas en archivos de imagen de alta calidad de forma rápida y sencilla para compartir y almacenar mejor.
type: docs
weight: 30
url: /es/net/aspose.words.lowcode/converter/converttoimages/
---
## ConvertToImages(*string, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_5}

Convierte las páginas del archivo de entrada especificado en imágenes en el formato especificado y devuelve una matriz de secuencias que contienen las imágenes.

```csharp
public static Stream[] ConvertToImages(string inputFile, SaveFormat saveFormat)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFile | String | El nombre del archivo de entrada. |
| saveFormat | SaveFormat | Formato de guardado. Solo se permiten formatos de guardado de imagen. |

### Valor_devuelto

Devuelve una matriz de secuencias de imágenes. El usuario final debe gestionar las secuencias.

## Ejemplos

Muestra cómo convertir documentos a secuencias de imágenes.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## ConvertToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_6}

Convierte las páginas del archivo de entrada especificado en imágenes utilizando las opciones de guardado especificadas y devuelve una matriz de secuencias que contienen las imágenes.

```csharp
public static Stream[] ConvertToImages(string inputFile, ImageSaveOptions saveOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFile | String | El nombre del archivo de entrada. |
| saveOptions | ImageSaveOptions | Opciones para guardar imágenes. |

### Valor_devuelto

Devuelve una matriz de secuencias de imágenes. El usuario final debe gestionar las secuencias.

## Ejemplos

Muestra cómo convertir documentos a secuencias de imágenes.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_3}

Convierte las páginas del flujo de entrada especificado en imágenes en el formato especificado y devuelve una matriz de flujos que contienen las imágenes.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, SaveFormat saveFormat)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de entrada. |
| saveFormat | SaveFormat | Formato de guardado. Solo se permiten formatos de guardado de imagen. |

### Valor_devuelto

Devuelve una matriz de secuencias de imágenes. El usuario final debe gestionar las secuencias.

## Ejemplos

Muestra cómo convertir documentos a imágenes desde una secuencia.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_4}

Convierte las páginas del flujo de entrada especificado en imágenes utilizando las opciones de guardado especificadas y devuelve una matriz de flujos que contienen las imágenes.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, ImageSaveOptions saveOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de entrada. |
| saveOptions | ImageSaveOptions | Opciones para guardar imágenes. |

### Valor_devuelto

Devuelve una matriz de secuencias de imágenes. El usuario final debe gestionar las secuencias.

## Ejemplos

Muestra cómo convertir documentos a imágenes desde una secuencia.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_2}

Convierte las páginas del flujo de entrada especificado en imágenes utilizando las opciones de carga y guardado proporcionadas, y devuelve una matriz de flujos que contienen las imágenes.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, LoadOptions loadOptions, 
    ImageSaveOptions saveOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de entrada. |
| loadOptions | LoadOptions | Las opciones de carga del documento de entrada. |
| saveOptions | ImageSaveOptions | Opciones para guardar imágenes. |

### Valor_devuelto

Devuelve una matriz de secuencias de imágenes. El usuario final debe gestionar las secuencias.

## Ejemplos

Muestra cómo convertir documentos a imágenes desde una secuencia.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Ver también

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## ConvertToImages(*[Document](../../../aspose.words/document/), [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages}

Convierte las páginas del documento especificado en imágenes en el formato especificado y devuelve una matriz de secuencias que contienen las imágenes.

```csharp
public static Stream[] ConvertToImages(Document doc, SaveFormat saveFormat)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | Document | El documento de entrada. |
| saveFormat | SaveFormat | Formato de guardado. Solo se permiten formatos de guardado de imagen. |

### Valor_devuelto

Devuelve una matriz de secuencias de imágenes. El usuario final debe gestionar las secuencias.

## Ejemplos

Muestra cómo convertir documentos a secuencias de imágenes.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Ver también

* class [Document](../../../aspose.words/document/)
* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## ConvertToImages(*[Document](../../../aspose.words/document/), [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_1}

Convierte las páginas del documento especificado en imágenes utilizando las opciones de guardado especificadas y devuelve una matriz de secuencias que contienen las imágenes.

```csharp
public static Stream[] ConvertToImages(Document doc, ImageSaveOptions saveOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| doc | Document | El documento de entrada. |
| saveOptions | ImageSaveOptions | Opciones para guardar imágenes. |

### Valor_devuelto

Devuelve una matriz de secuencias de imágenes. El usuario final debe gestionar las secuencias.

## Ejemplos

Muestra cómo convertir documentos a secuencias de imágenes.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Ver también

* class [Document](../../../aspose.words/document/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
