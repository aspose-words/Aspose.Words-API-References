---
title: Watermark.SetImage
second_title: Referencia de API de Aspose.Words para .NET
description: Watermark método. Agrega una marca de agua de imagen al documento.
type: docs
weight: 30
url: /es/net/aspose.words/watermark/setimage/
---
## SetImage(Image) {#setimage}

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

### Ver también

* class [Watermark](../)
* espacio de nombres [Aspose.Words](../../watermark/)
* asamblea [Aspose.Words](../../../)

---

## SetImage(Image, ImageWatermarkOptions) {#setimage_1}

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

### Observaciones

Si[`ImageWatermarkOptions`](../../imagewatermarkoptions/) es`nulo`, la marca de agua se configurará con las opciones predeterminadas.

### Ejemplos

Muestra cómo crear una marca de agua a partir de una imagen en el sistema de archivos local.

```csharp
Document doc = new Document();

            // Modifica la apariencia de la marca de agua de la imagen con un objeto ImageWatermarkOptions,
            // luego pásalo mientras creas una marca de agua a partir de un archivo de imagen.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET48 || JAVA
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);
#elif NET5_0_OR_GREATER || __MOBILE__
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
* espacio de nombres [Aspose.Words](../../watermark/)
* asamblea [Aspose.Words](../../../)

---

## SetImage(string, ImageWatermarkOptions) {#setimage_2}

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
| ArgumentNullException | Lanza cuando la ruta es`nulo` . |

### Observaciones

Si[`ImageWatermarkOptions`](../../imagewatermarkoptions/) es`nulo`, la marca de agua se configurará con las opciones predeterminadas.

### Ver también

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* espacio de nombres [Aspose.Words](../../watermark/)
* asamblea [Aspose.Words](../../../)


