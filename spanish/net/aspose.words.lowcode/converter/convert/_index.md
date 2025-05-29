---
title: Converter.Convert
linktitle: Convert
articleTitle: Convert
second_title: Aspose.Words para .NET
description: Convierte tus documentos fácilmente con el método Convert de nuestro conversor. Transforma los archivos de entrada a los formatos que desees con facilidad y precisión.
type: docs
weight: 20
url: /es/net/aspose.words.lowcode/converter/convert/
---
## Convert(*string, string*) {#convert_4}

Convierte el documento de entrada dado en el documento de salida utilizando los nombres de archivo de entrada y salida especificados y sus extensiones.

```csharp
public static void Convert(string inputFile, string outputFile)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFile | String | El nombre del archivo de entrada. |
| outputFile | String | El nombre del archivo de salida. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ejemplos

Muestra cómo convertir documentos con una sola línea de código.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Ver también

* class [Converter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## Convert(*string, string, [SaveFormat](../../../aspose.words/saveformat/)*) {#convert_5}

Convierte el documento de entrada dado en el documento de salida utilizando los nombres de archivo de entrada y salida especificados y el formato del documento final.

```csharp
public static void Convert(string inputFile, string outputFile, SaveFormat saveFormat)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFile | String | El nombre del archivo de entrada. |
| outputFile | String | El nombre del archivo de salida. |
| saveFormat | SaveFormat | El formato de guardado. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ejemplos

Muestra cómo convertir documentos con una sola línea de código.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## Convert(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_6}

Convierte el documento de entrada dado en el documento de salida utilizando los nombres de archivo de entrada y salida especificados y las opciones de guardado.

```csharp
public static void Convert(string inputFile, string outputFile, SaveOptions saveOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFile | String | El nombre del archivo de entrada. |
| outputFile | String | El nombre del archivo de salida. |
| saveOptions | SaveOptions | Las opciones de guardado. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ejemplos

Muestra cómo convertir documentos con una sola línea de código.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## Convert(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/), string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_3}

Convierte el documento de entrada dado en el documento de salida utilizando los nombres de archivo de entrada y salida especificados y sus opciones de carga y guardado.

```csharp
public static void Convert(string inputFile, LoadOptions loadOptions, string outputFile, 
    SaveOptions saveOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFile | String | El nombre del archivo de entrada. |
| loadOptions | LoadOptions | Las opciones de carga del documento de entrada. |
| outputFile | String | El nombre del archivo de salida. |
| saveOptions | SaveOptions | Las opciones de guardado. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ejemplos

Muestra cómo convertir documentos con una sola línea de código.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Ver también

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## Convert(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#convert_1}

Convierte el documento de entrada dado en un único documento de salida utilizando flujos de entrada y salida especificados.

```csharp
public static void Convert(Stream inputStream, Stream outputStream, SaveFormat saveFormat)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de entrada. |
| outputStream | Stream | El flujo de salida. |
| saveFormat | SaveFormat | El formato de guardado. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo se guardará la primera página de la salida en la secuencia especificada.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en la secuencia especificada.

## Ejemplos

Muestra cómo convertir documentos con una sola línea de código (Stream).

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## Convert(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_2}

Convierte el documento de entrada dado en un único documento de salida utilizando flujos de entrada y salida especificados.

```csharp
public static void Convert(Stream inputStream, Stream outputStream, SaveOptions saveOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | Los flujos de entrada. |
| outputStream | Stream | El flujo de salida. |
| saveOptions | SaveOptions | Las opciones de guardado. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo se guardará la primera página de la salida en la secuencia especificada.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en la secuencia especificada.

## Ejemplos

Muestra cómo convertir documentos con una sola línea de código (Stream).

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## Convert(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/), Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert}

Convierte el documento de entrada dado en un único documento de salida utilizando flujos de entrada y salida especificados.

```csharp
public static void Convert(Stream inputStream, LoadOptions loadOptions, Stream outputStream, 
    SaveOptions saveOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | Los flujos de entrada. |
| loadOptions | LoadOptions | Las opciones de carga del documento de entrada. |
| outputStream | Stream | El flujo de salida. |
| saveOptions | SaveOptions | Las opciones de guardado. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo se guardará la primera página de la salida en la secuencia especificada.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en la secuencia especificada.

## Ejemplos

Muestra cómo convertir documentos con una sola línea de código (Stream).

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### Ver también

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
