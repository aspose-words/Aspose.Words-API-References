---
title: Watermarker.SetWatermarkToImages
linktitle: SetWatermarkToImages
articleTitle: SetWatermarkToImages
second_title: Aspose.Words para .NET
description: Mejore sus imágenes con nuestro método Watermarker Set, agregando marcas de agua de texto personalizables para lograr un toque profesional y un resultado perfecto.
type: docs
weight: 40
url: /es/net/aspose.words.lowcode/watermarker/setwatermarktoimages/
---
## SetWatermarkToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#setwatermarktoimages_3}

Agrega una marca de agua de texto al documento con opciones. Representa la salida en imágenes.

```csharp
public static Stream[] SetWatermarkToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| saveOptions | ImageSaveOptions | Las opciones de guardado. |
| watermarkText | String | Texto que se muestra como marca de agua. |
| options | TextWatermarkOptions | Define opciones adicionales para la marca de agua de texto. |

## Ejemplos

Muestra cómo insertar texto de marca de agua en el documento y guardar el resultado en imágenes.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Stream[] images = Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), watermarkText);

TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
images = Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), watermarkText, watermarkOptions);
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## SetWatermarkToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#setwatermarktoimages_1}

Agrega una marca de agua de texto al documento con opciones. Representa la salida en imágenes.

```csharp
public static Stream[] SetWatermarkToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de archivo de entrada. |
| saveOptions | ImageSaveOptions | Las opciones de guardado. |
| watermarkText | String | Texto que se muestra como marca de agua. |
| options | TextWatermarkOptions | Define opciones adicionales para la marca de agua de texto. |

## Ejemplos

Muestra cómo insertar texto de marca de agua en el documento desde la secuencia y guardar el resultado en imágenes.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), watermarkText);

    TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
    watermarkOptions.Color = Color.Red;
    images = Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), watermarkText, watermarkOptions);
}
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## SetWatermarkToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), byte[], [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setwatermarktoimages_2}

Agrega una marca de agua de imagen al documento con opciones. Representa la salida en imágenes.

```csharp
public static Stream[] SetWatermarkToImages(string inputFileName, ImageSaveOptions saveOptions, 
    byte[] watermarkImageBytes, ImageWatermarkOptions options = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| saveOptions | ImageSaveOptions | Las opciones de guardado. |
| watermarkImageBytes | Byte[] | Bytes de imagen que se muestran como marca de agua. |
| options | ImageWatermarkOptions | Define opciones adicionales para la marca de agua de la imagen. |

## Ejemplos

Muestra cómo insertar una imagen de marca de agua en el documento y guardar el resultado en imágenes.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), File.ReadAllBytes(watermarkImage));

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), File.ReadAllBytes(watermarkImage), options);
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## SetWatermarkToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Stream, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setwatermarktoimages}

Agrega una marca de agua de imagen al documento con opciones. Representa la salida en imágenes.

```csharp
public static Stream[] SetWatermarkToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    Stream watermarkImageStream, ImageWatermarkOptions options = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de entrada. |
| saveOptions | ImageSaveOptions | Las opciones de guardado. |
| watermarkImageStream | Stream | Flujo de imágenes que se muestra como marca de agua. |
| options | ImageWatermarkOptions | Define opciones adicionales para la marca de agua de la imagen. |

## Ejemplos

Muestra cómo insertar una imagen de marca de agua en el documento desde una secuencia y guardar el resultado en imágenes.

```csharp
string watermarkImage = ImageDir + "Logo.jpg";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream imageStream = new FileStream(watermarkImage, FileMode.Open, FileAccess.Read))
    {
        Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), imageStream);
        Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), imageStream, new ImageWatermarkOptions() { Scale = 50 });
    }
}
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
