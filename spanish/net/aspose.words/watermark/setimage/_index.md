---
title: Watermark.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words para .NET
description: Mejore sus documentos con el método SetImage de marca de agua. Añada fácilmente marcas de agua de imagen impactantes para un toque profesional.
type: docs
weight: 30
url: /es/net/aspose.words/watermark/setimage/
---
## SetImage(*Image*) {#setimage}

Agrega una marca de agua de imagen al documento.

```csharp
public void SetImage(Image image)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| image | Image | Imagen que se muestra como marca de agua. |

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentNullException | Se lanza cuando la imagen es`nulo` . |

## Ejemplos

Muestra cómo crear una marca de agua a partir de una imagen en el sistema de archivos local.

```csharp
Document doc = new Document();

            // Modifique la apariencia de la marca de agua de la imagen con un objeto ImageWatermarkOptions,
            // luego pásalo mientras creas una marca de agua a partir de un archivo de imagen.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            //Tenemos diferentes opciones para insertar imágenes:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Ver también

* class [Watermark](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## SetImage(*Image, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_1}

Agrega una marca de agua de imagen al documento.

```csharp
public void SetImage(Image image, ImageWatermarkOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| image | Image | Imagen que se muestra como marca de agua. |
| options | ImageWatermarkOptions | Define opciones adicionales para la marca de agua de la imagen. |

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentNullException | Se lanza cuando la imagen es`nulo` . |

## Observaciones

Si[`ImageWatermarkOptions`](../../imagewatermarkoptions/) es`nulo`, la marca de agua se establecerá con las opciones predeterminadas.

## Ejemplos

Muestra cómo crear una marca de agua a partir de una imagen en el sistema de archivos local.

```csharp
Document doc = new Document();

            // Modifique la apariencia de la marca de agua de la imagen con un objeto ImageWatermarkOptions,
            // luego pásalo mientras creas una marca de agua a partir de un archivo de imagen.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            //Tenemos diferentes opciones para insertar imágenes:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Ver también

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## SetImage(*string, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_3}

Agrega una marca de agua de imagen al documento.

```csharp
public void SetImage(string imagePath, ImageWatermarkOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| imagePath | String | Ruta al archivo de imagen que se muestra como marca de agua. |
| options | ImageWatermarkOptions | Define opciones adicionales para la marca de agua de la imagen. |

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentNullException | Se lanza cuando la ruta es`nulo` . |

## Observaciones

Si[`ImageWatermarkOptions`](../../imagewatermarkoptions/) es`nulo`, la marca de agua se establecerá con las opciones predeterminadas.

## Ejemplos

Muestra cómo crear una marca de agua a partir de una imagen en el sistema de archivos local.

```csharp
Document doc = new Document();

            // Modifique la apariencia de la marca de agua de la imagen con un objeto ImageWatermarkOptions,
            // luego pásalo mientras creas una marca de agua a partir de un archivo de imagen.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            //Tenemos diferentes opciones para insertar imágenes:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Ver también

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## SetImage(*Stream, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_2}

Agrega una marca de agua de imagen al documento.

```csharp
public void SetImage(Stream imageStream, ImageWatermarkOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| imageStream | Stream | La secuencia que contiene los datos de la imagen que se muestran como marca de agua. |
| options | ImageWatermarkOptions | Define opciones adicionales para la marca de agua de la imagen. |

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentNullException | Se lanza cuando la ruta es`nulo` . |

## Observaciones

Si[`ImageWatermarkOptions`](../../imagewatermarkoptions/) es`nulo`, la marca de agua se establecerá con las opciones predeterminadas.

## Ejemplos

Muestra cómo crear una marca de agua a partir de un flujo de imágenes.

```csharp
Document doc = new Document();

// Modifique la apariencia de la marca de agua de la imagen con un objeto ImageWatermarkOptions,
// luego pásalo mientras creas una marca de agua a partir de un archivo de imagen.
ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
imageWatermarkOptions.Scale = 5;

using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
    doc.Watermark.SetImage(imageStream, imageWatermarkOptions);

doc.Save(ArtifactsDir + "Document.ImageWatermarkStream.docx");
```

### Ver también

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
