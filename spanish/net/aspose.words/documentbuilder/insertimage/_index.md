---
title: DocumentBuilder.InsertImage
linktitle: InsertImage
articleTitle: InsertImage
second_title: Aspose.Words para .NET
description: DocumentBuilder InsertImage método. Inserta una imagen desde un .NETImage objeto en el documento. La imagen se inserta en línea y a escala del 100 en C#.
type: docs
weight: 370
url: /es/net/aspose.words/documentbuilder/insertimage/
---
## InsertImage(*Image*) {#insertimage_3}

Inserta una imagen desde un .NETImage objeto en el documento. La imagen se inserta en línea y a escala del 100%.

```csharp
public Shape InsertImage(Image image)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| image | Image | La imagen a insertar en el documento. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

## Ejemplos

Muestra cómo insertar una imagen de un objeto en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// A continuación se muestran tres formas de insertar una imagen desde una instancia de objeto Imagen.
// 1 - Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forma en línea con dimensiones personalizadas:
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forma flotante con dimensiones personalizadas:
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertImage(*string*) {#insertimage_9}

Inserta una imagen de un archivo o URL en el documento. La imagen se inserta en línea y a escala del 100%.

```csharp
public Shape InsertImage(string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | El archivo con la imagen. Puede ser cualquier URI local o remoto válido. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Esta sobrecarga descargará automáticamente la imagen antes de insertarla en document si especifica un URI remoto.

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

## Ejemplos

Muestra cómo insertar una imagen gif en el documento.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Podemos insertar una imagen gif usando la ruta o la matriz de bytes.
// Solo funciona si DocumentBuilder está optimizado para la versión 2010 o superior de Word.
// Tenga en cuenta que el acceso a los bytes de la imagen provoca la conversión de Gif a Png.
Shape gifImage = builder.InsertImage(ImageDir + "Graphics Interchange Format.gif");

gifImage = builder.InsertImage(File.ReadAllBytes(ImageDir + "Graphics Interchange Format.gif"));

builder.Document.Save(ArtifactsDir + "InsertGif.docx");
```

Muestra cómo insertar una forma con una imagen en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación se muestran dos ubicaciones donde se encuentra el método "InsertShape" del generador de documentos.
// puede obtener la imagen que mostrará la forma.
// 1 - Pasar un nombre de archivo del sistema de archivos local de un archivo de imagen:
builder.Write("Image from local file: ");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.Writeln();

// 2 - Pasa una URL que apunte a una imagen.
builder.Write("Image from a URL: ");
builder.InsertImage(ImageUrl);
builder.Writeln();

doc.Save(ArtifactsDir + "Image.FromUrl.docx");
```

Muestra cómo insertar una imagen flotante en el centro de una página.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta una imagen flotante que aparecerá detrás del texto superpuesto y alinéala con el centro de la página.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Muestra cómo determinar qué imagen se insertará.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Scalable Vector Graphics.svg");

// Aspose.Words inserta una imagen SVG en el documento como PNG con la extensión svgBlip
// que contiene la representación de la imagen vectorial SVG original.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words inserta una imagen SVG en el documento como PNG, tal como lo hace Microsoft Word con el formato anterior.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);

// Aspose.Words inserta una imagen SVG en el documento como metarchivo EMF para mantener la imagen en representación vectorial.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Emf.docx");
```

Muestra cómo insertar una imagen del sistema de archivos local en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación se muestran tres formas de insertar una imagen desde un nombre de archivo del sistema local.
// 1 - Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forma en línea con dimensiones personalizadas:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forma flotante con dimensiones personalizadas:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertImage(*Stream*) {#insertimage_6}

Inserta una imagen de una secuencia en el documento. La imagen se inserta en línea y a escala del 100%.

```csharp
public Shape InsertImage(Stream stream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | La secuencia que contiene la imagen. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

## Ejemplos

Muestra cómo insertar una forma con una imagen de una secuencia en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    builder.Write("Image from stream: ");
    builder.InsertImage(stream);
}

doc.Save(ArtifactsDir + "Image.FromStream.docx");
```

Muestra cómo insertar una imagen de una secuencia en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // A continuación se muestran tres formas de insertar una imagen desde una secuencia.
    // 1 - Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forma en línea con dimensiones personalizadas:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forma flotante con dimensiones personalizadas:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertImage(*byte[]*) {#insertimage}

Inserta una imagen de una matriz de bytes en el documento. La imagen se inserta en línea y a escala del 100%.

```csharp
public Shape InsertImage(byte[] imageBytes)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| imageBytes | Byte[] | La matriz de bytes que contiene la imagen. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

## Ejemplos

Muestra cómo insertar una imagen de una matriz de bytes en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // A continuación se muestran tres formas de insertar una imagen desde una matriz de bytes.
    // 1 - Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forma en línea con dimensiones personalizadas:
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forma flotante con dimensiones personalizadas:
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

Muestra cómo insertar una imagen de una matriz de bytes en un documento (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Decodificar la imagen la convertirá al formato .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // A continuación se muestran tres formas de insertar una imagen desde una matriz de bytes.
            // 1 - Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - Forma en línea con dimensiones personalizadas:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - Forma flotante con dimensiones personalizadas:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertImage(*Image, double, double*) {#insertimage_5}

Inserta una imagen en línea desde .NETImage objeto en el documento y lo escala al tamaño especificado.

```csharp
public Shape InsertImage(Image image, double width, double height)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| image | Image | La imagen a insertar en el documento. |
| width | Double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| height | Double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

## Ejemplos

Muestra cómo insertar una imagen de un objeto en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// A continuación se muestran tres formas de insertar una imagen desde una instancia de objeto Imagen.
// 1 - Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forma en línea con dimensiones personalizadas:
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forma flotante con dimensiones personalizadas:
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

Muestra cómo insertar una imagen de un objeto en un documento (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Decodificar la imagen la convertirá al formato .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    // A continuación se muestran tres formas de insertar una imagen desde una instancia de objeto Imagen.
    // 1 - Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
    builder.InsertImage(bitmap);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forma en línea con dimensiones personalizadas:
    builder.InsertImage(bitmap, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forma flotante con dimensiones personalizadas:
    builder.InsertImage(bitmap, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObjectNetStandard2.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertImage(*string, double, double*) {#insertimage_11}

Inserta una imagen en línea de un archivo o URL en el documento y la escala al tamaño especificado.

```csharp
public Shape InsertImage(string fileName, double width, double height)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | El archivo que contiene la imagen. |
| width | Double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| height | Double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

## Ejemplos

Muestra cómo insertar una imagen del sistema de archivos local en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación se muestran tres formas de insertar una imagen desde un nombre de archivo del sistema local.
// 1 - Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forma en línea con dimensiones personalizadas:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forma flotante con dimensiones personalizadas:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertImage(*Stream, double, double*) {#insertimage_8}

Inserta una imagen en línea de una secuencia en el documento y la escala al tamaño especificado.

```csharp
public Shape InsertImage(Stream stream, double width, double height)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | La secuencia que contiene la imagen. |
| width | Double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| height | Double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

## Ejemplos

Muestra cómo insertar una imagen de una secuencia en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // A continuación se muestran tres formas de insertar una imagen desde una secuencia.
    // 1 - Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forma en línea con dimensiones personalizadas:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forma flotante con dimensiones personalizadas:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertImage(*byte[], double, double*) {#insertimage_2}

Inserta una imagen en línea de una matriz de bytes en el documento y la escala al tamaño especificado.

```csharp
public Shape InsertImage(byte[] imageBytes, double width, double height)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| imageBytes | Byte[] | La matriz de bytes que contiene la imagen. |
| width | Double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| height | Double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

## Ejemplos

Muestra cómo insertar una imagen de una matriz de bytes en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // A continuación se muestran tres formas de insertar una imagen desde una matriz de bytes.
    // 1 - Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forma en línea con dimensiones personalizadas:
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forma flotante con dimensiones personalizadas:
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

Muestra cómo insertar una imagen de una matriz de bytes en un documento (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Decodificar la imagen la convertirá al formato .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // A continuación se muestran tres formas de insertar una imagen desde una matriz de bytes.
            // 1 - Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - Forma en línea con dimensiones personalizadas:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - Forma flotante con dimensiones personalizadas:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertImage(*Image, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_4}

Inserta una imagen desde un .NETImage objeto en la posición y tamaño especificados.

```csharp
public Shape InsertImage(Image image, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| image | Image | La imagen a insertar en el documento. |
| horzPos | RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| left | Double | Distancia en puntos desde el origen hasta el lado izquierdo de la imagen. |
| vertPos | RelativeVerticalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| top | Double | Distancia en puntos desde el origen hasta la parte superior de la imagen. |
| width | Double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| height | Double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| wrapType | WrapType | Especifica cómo ajustar el texto alrededor de la imagen. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

## Ejemplos

Muestra cómo insertar una imagen de un objeto en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

// A continuación se muestran tres formas de insertar una imagen desde una instancia de objeto Imagen.
// 1 - Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
builder.InsertImage(image);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forma en línea con dimensiones personalizadas:
builder.InsertImage(image, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forma flotante con dimensiones personalizadas:
builder.InsertImage(image, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

Muestra cómo insertar una imagen de un objeto en un documento (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Decodificar la imagen la convertirá al formato .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    // A continuación se muestran tres formas de insertar una imagen desde una instancia de objeto Imagen.
    // 1 - Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
    builder.InsertImage(bitmap);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forma en línea con dimensiones personalizadas:
    builder.InsertImage(bitmap, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forma flotante con dimensiones personalizadas:
    builder.InsertImage(bitmap, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObjectNetStandard2.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertImage(*string, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_10}

Inserta una imagen de un archivo o URL en la posición y tamaño especificados.

```csharp
public Shape InsertImage(string fileName, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | El archivo que contiene la imagen. |
| horzPos | RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| left | Double | Distancia en puntos desde el origen hasta el lado izquierdo de la imagen. |
| vertPos | RelativeVerticalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| top | Double | Distancia en puntos desde el origen hasta la parte superior de la imagen. |
| width | Double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| height | Double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| wrapType | WrapType | Especifica cómo ajustar el texto alrededor de la imagen. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

## Ejemplos

Muestra cómo insertar una imagen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Hay dos formas de utilizar un generador de documentos para obtener una imagen y luego insertarla como una forma flotante.
// 1 - Desde un archivo en el sistema de archivos local:
builder.InsertImage(ImageDir + "Transparent background logo.png", RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 0, 200, 200, WrapType.Square);

// 2 - Desde una URL:
builder.InsertImage(ImageUrl, RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 250, 200, 200, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFloatingImage.docx");
```

Muestra cómo insertar una imagen del sistema de archivos local en un documento conservando sus dimensiones.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// El método InsertImage crea una forma flotante con la imagen pasada en sus datos de imagen.
// Podemos especificar las dimensiones de la forma, pasándolas a este método.
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg", RelativeHorizontalPosition.Margin, 0,
    RelativeVerticalPosition.Margin, 0, -1, -1, WrapType.Square);

// Pasar valores negativos como las dimensiones deseadas definirá automáticamente
// las dimensiones de la forma según las dimensiones de su imagen.
Assert.AreEqual(300.0d, imageShape.Width);
Assert.AreEqual(300.0d, imageShape.Height);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertImageOriginalSize.docx");
```

Muestra cómo insertar una imagen del sistema de archivos local en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación se muestran tres formas de insertar una imagen desde un nombre de archivo del sistema local.
// 1 - Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Forma en línea con dimensiones personalizadas:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Forma flotante con dimensiones personalizadas:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertImage(*Stream, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_7}

Inserta una imagen de una secuencia en la posición y el tamaño especificados.

```csharp
public Shape InsertImage(Stream stream, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | La secuencia que contiene la imagen. |
| horzPos | RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| left | Double | Distancia en puntos desde el origen hasta el lado izquierdo de la imagen. |
| vertPos | RelativeVerticalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| top | Double | Distancia en puntos desde el origen hasta la parte superior de la imagen. |
| width | Double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| height | Double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| wrapType | WrapType | Especifica cómo ajustar el texto alrededor de la imagen. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

## Ejemplos

Muestra cómo insertar una imagen de una secuencia en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // A continuación se muestran tres formas de insertar una imagen desde una secuencia.
    // 1 - Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forma en línea con dimensiones personalizadas:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forma flotante con dimensiones personalizadas:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertImage(*byte[], [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_1}

Inserta una imagen de una matriz de bytes en la posición y el tamaño especificados.

```csharp
public Shape InsertImage(byte[] imageBytes, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| imageBytes | Byte[] | La matriz de bytes que contiene la imagen. |
| horzPos | RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| left | Double | Distancia en puntos desde el origen hasta el lado izquierdo de la imagen. |
| vertPos | RelativeVerticalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| top | Double | Distancia en puntos desde el origen hasta la parte superior de la imagen. |
| width | Double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| height | Double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| wrapType | WrapType | Especifica cómo ajustar el texto alrededor de la imagen. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

## Ejemplos

Muestra cómo insertar una imagen de una matriz de bytes en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Image image = Image.FromFile(ImageDir + "Logo.jpg");

using (MemoryStream ms = new MemoryStream())
{
    image.Save(ms, ImageFormat.Png);
    byte[] imageByteArray = ms.ToArray();

    // A continuación se muestran tres formas de insertar una imagen desde una matriz de bytes.
    // 1 - Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
    builder.InsertImage(imageByteArray);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Forma en línea con dimensiones personalizadas:
    builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Forma flotante con dimensiones personalizadas:
    builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin, 
    100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

Muestra cómo insertar una imagen de una matriz de bytes en un documento (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Decodificar la imagen la convertirá al formato .png.
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
{
    using (SKImage image = SKImage.FromBitmap(bitmap))
    {
        using (SKData data = image.Encode())
        {
            byte[] imageByteArray = data.ToArray();

            // A continuación se muestran tres formas de insertar una imagen desde una matriz de bytes.
            // 1 - Forma en línea con un tamaño predeterminado basado en las dimensiones originales de la imagen:
            builder.InsertImage(imageByteArray);

            builder.InsertBreak(BreakType.PageBreak);

            // 2 - Forma en línea con dimensiones personalizadas:
            builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

            builder.InsertBreak(BreakType.PageBreak);

            // 3 - Forma flotante con dimensiones personalizadas:
            builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
                100, 200, 100, WrapType.Square);
        }
    }
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArrayNetStandard2.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
