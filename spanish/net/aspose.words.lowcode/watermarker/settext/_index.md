---
title: Watermarker.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words para .NET
description: Mejore sus documentos con nuestro método SetText de Marcadores de Agua. Añada fácilmente marcas de agua de texto personalizables para mejorar su imagen de marca y profesionalismo.
type: docs
weight: 30
url: /es/net/aspose.words.lowcode/watermarker/settext/
---
## SetText(*string, string, string*) {#settext_4}

Agrega una marca de agua de texto al documento.

```csharp
public static void SetText(string inputFileName, string outputFileName, string watermarkText)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |
| watermarkText | String | Texto que se muestra como marca de agua. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ejemplos

Muestra cómo insertar texto de marca de agua en el documento.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### Ver también

* class [Watermarker](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## SetText(*string, string, string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_5}

Agrega una marca de agua de texto al documento con opciones.

```csharp
public static void SetText(string inputFileName, string outputFileName, string watermarkText, 
    TextWatermarkOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |
| watermarkText | String | Texto que se muestra como marca de agua. |
| options | TextWatermarkOptions | Define opciones adicionales para la marca de agua de texto. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ejemplos

Muestra cómo insertar texto de marca de agua en el documento.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### Ver también

* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## SetText(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_2}

Agrega una marca de agua de texto al documento con opciones y formato de guardado especificado.

```csharp
public static void SetText(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |
| saveFormat | SaveFormat | El formato de guardado. |
| watermarkText | String | Texto que se muestra como marca de agua. |
| options | TextWatermarkOptions | Define opciones adicionales para la marca de agua de texto. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ejemplos

Muestra cómo insertar texto de marca de agua en el documento.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## SetText(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_3}

Agrega una marca de agua de texto al documento con opciones y formato de guardado especificado.

```csharp
public static void SetText(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |
| saveOptions | SaveOptions | Las opciones de guardado. |
| watermarkText | String | Texto que se muestra como marca de agua. |
| options | TextWatermarkOptions | Define opciones adicionales para la marca de agua de texto. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## SetText(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext}

Agrega una marca de agua de texto al documento desde secuencias con opciones.

```csharp
public static void SetText(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de entrada. |
| outputStream | Stream | El flujo de salida. |
| saveFormat | SaveFormat | El formato de guardado. |
| watermarkText | String | Texto que se muestra como marca de agua. |
| options | TextWatermarkOptions | Define opciones adicionales para la marca de agua de texto. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo se guardará la primera página de la salida en la secuencia especificada.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en la secuencia especificada.

## Ejemplos

Muestra cómo insertar texto de marca de agua en el documento desde la secuencia.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkTextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.SetText(streamIn, streamOut, SaveFormat.Docx, watermarkText);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkTextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
    {
        TextWatermarkOptions options = new TextWatermarkOptions();
        options.Color = Color.Red;
        Watermarker.SetText(streamIn, streamOut, SaveFormat.Docx, watermarkText, options);
    }
}
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## SetText(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_1}

Agrega una marca de agua de texto al documento desde secuencias con opciones.

```csharp
public static void SetText(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de entrada. |
| outputStream | Stream | El flujo de salida. |
| saveOptions | SaveOptions | Las opciones de guardado. |
| watermarkText | String | Texto que se muestra como marca de agua. |
| options | TextWatermarkOptions | Define opciones adicionales para la marca de agua de texto. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo se guardará la primera página de la salida en la secuencia especificada.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en la secuencia especificada.

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
