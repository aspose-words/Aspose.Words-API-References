---
title: InsertOnlineVideo
second_title: Referencia de API de Aspose.Words para .NET
description: Inserta un objeto de video en línea en el documento y lo escala al tamaño especificado.
type: docs
weight: 390
url: /es/net/aspose.words/documentbuilder/insertonlinevideo/
---
## InsertOnlineVideo(string, double, double) {#insertonlinevideo_1}

Inserta un objeto de video en línea en el documento y lo escala al tamaño especificado.

```csharp
public Shape InsertOnlineVideo(string videoUrl, double width, double height)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| videoUrl | String | La URL del video. |
| width | Double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| height | Double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

### Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

Se admite la inserción de videos en línea de los siguientes recursos:

* https://www.youtube.com/
* https://vimeo.com/

Si su video en línea no se muestra correctamente, use`InsertOnlineVideo`, que acepta código html incrustado personalizado.

El código para incrustar video puede variar entre proveedores, consulte a su proveedor de elección correspondiente para obtener más detalles.

### Ejemplos

Muestra cómo insertar un video en línea en un documento usando una URL.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOnlineVideo("https://youtu.be/t_1LYZ102RA", 360, 270);

// Podemos ver el video desde Microsoft Word haciendo clic en la forma.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertVideoWithUrl.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertonlinevideo}

Inserta un objeto de video en línea en el documento y lo escala al tamaño especificado.

```csharp
public Shape InsertOnlineVideo(string videoUrl, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| videoUrl | String | La URL del video. |
| horzPos | RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| left | Double | Distancia en puntos desde el origen hasta el lado izquierdo de la imagen. |
| vertPos | RelativeVerticalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| top | Double | Distancia en puntos desde el origen hasta el lado superior de la imagen. |
| width | Double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| height | Double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| wrapType | WrapType | Especifica cómo ajustar el texto alrededor de la imagen. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

### Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

Se admite la inserción de videos en línea de los siguientes recursos:

* https://www.youtube.com/
* https://vimeo.com/

Si su video en línea no se muestra correctamente, use`InsertOnlineVideo`, que acepta código html incrustado personalizado.

El código para incrustar video puede variar entre proveedores, consulte a su proveedor de elección correspondiente para obtener más detalles.

### Ejemplos

Muestra cómo insertar un video en línea en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";

// Inserte una forma que reproduzca un video de la web cuando se haga clic en Microsoft Word.
// Esta forma rectangular contendrá una imagen basada en el primer cuadro del video vinculado
// y un indicador visual de "botón de reproducción". El video tiene una relación de aspecto de 16:9.
// Ajustaremos el tamaño de la forma a esa proporción, para que la imagen no aparezca estirada.
builder.InsertOnlineVideo(videoUrl, RelativeHorizontalPosition.LeftMargin, 0,
    RelativeVerticalPosition.TopMargin, 0, 320, 180, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideo.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, string, byte[], double, double) {#insertonlinevideo_3}

Inserta un objeto de video en línea en el documento y lo escala al tamaño especificado.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    double width, double height)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| videoUrl | String | La URL del video. |
| videoEmbedCode | String | El código de inserción para el video. |
| thumbnailImageBytes | Byte[] | Los bytes de la imagen en miniatura. |
| width | Double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| height | Double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

### Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

### Ejemplos

Muestra cómo insertar un video en línea en un documento con una miniatura personalizada.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" ancho=\"640\" alto=\"360\" marcoborder=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // A continuación se muestran dos formas de crear una forma con una miniatura personalizada, que enlaza con un video en línea
        // que se reproducirá cuando hagamos clic en la forma en Microsoft Word.
        // 1 - Insertar una forma en línea en el cursor de inserción del nodo del constructor:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - Inserta una forma flotante:
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)

---

## InsertOnlineVideo(string, string, byte[], RelativeHorizontalPosition, double, RelativeVerticalPosition, double, double, double, WrapType) {#insertonlinevideo_2}

Inserta un objeto de video en línea en el documento y lo escala al tamaño especificado.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    double width, double height, WrapType wrapType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| videoUrl | String | La URL del video. |
| videoEmbedCode | String | El código de inserción para el video. |
| thumbnailImageBytes | Byte[] | Los bytes de la imagen en miniatura. |
| horzPos | RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| left | Double | Distancia en puntos desde el origen hasta el lado izquierdo de la imagen. |
| vertPos | RelativeVerticalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| top | Double | Distancia en puntos desde el origen hasta el lado superior de la imagen. |
| width | Double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| height | Double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| wrapType | WrapType | Especifica cómo ajustar el texto alrededor de la imagen. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

### Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

### Ejemplos

Muestra cómo insertar un video en línea en un documento con una miniatura personalizada.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" ancho=\"640\" alto=\"360\" marcoborder=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // A continuación se muestran dos formas de crear una forma con una miniatura personalizada, que enlaza con un video en línea
        // que se reproducirá cuando hagamos clic en la forma en Microsoft Word.
        // 1 - Insertar una forma en línea en el cursor de inserción del nodo del constructor:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - Inserta una forma flotante:
        double left = builder.PageSetup.RightMargin - image.Width;
        double top = builder.PageSetup.BottomMargin - image.Height;

        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes,
            RelativeHorizontalPosition.RightMargin, left, RelativeVerticalPosition.BottomMargin, top,
            image.Width, image.Height, WrapType.Square);
    }
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
