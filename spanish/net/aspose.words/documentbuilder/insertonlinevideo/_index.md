---
title: DocumentBuilder.InsertOnlineVideo
linktitle: InsertOnlineVideo
articleTitle: InsertOnlineVideo
second_title: Aspose.Words para .NET
description: Agregue y escale sin esfuerzo videos en línea en sus documentos con el método InsertOnlineVideo de DocumentBuilder para mejorar la participación y la creatividad.
type: docs
weight: 440
url: /es/net/aspose.words/documentbuilder/insertonlinevideo/
---
## InsertOnlineVideo(*string, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertonlinevideo}

Inserta un objeto de vídeo en línea en el documento y lo escala al tamaño especificado.

```csharp
public Shape InsertOnlineVideo(string videoUrl, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| videoUrl | String | La URL del vídeo. |
| horzPos | RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| left | Double | Distancia en puntos desde el origen hasta el lado izquierdo de la imagen. |
| vertPos | RelativeVerticalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| top | Double | Distancia en puntos desde el origen hasta la parte superior de la imagen. |
| width | Double | Ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100 %. |
| height | Double | Altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100 %. |
| wrapType | WrapType | Especifica cómo ajustar el texto alrededor de la imagen. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones utilizando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

Se admite la inserción de vídeos en línea desde los siguientes recursos:

* https://www.youtube.com/
* https://vimeo.com/

Si su video en línea no se muestra correctamente, utilice`InsertOnlineVideo`, que acepta código HTML incrustado personalizado.

El código para insertar vídeo puede variar entre proveedores; consulte con su proveedor correspondiente para obtener más detalles.

## Ejemplos

Muestra cómo insertar un vídeo en línea en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";

// Insertar una forma que reproduce un vídeo de la web cuando se hace clic en Microsoft Word.
// Esta forma rectangular contendrá una imagen basada en el primer fotograma del vídeo vinculado
// y un botón de reproducción. El vídeo tiene una relación de aspecto de 16:9.
// Estableceremos el tamaño de la forma en esa proporción, para que la imagen no aparezca estirada.
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
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, string, byte[], double, double*) {#insertonlinevideo_3}

Inserta un objeto de vídeo en línea en el documento y lo escala al tamaño especificado.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    double width, double height)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| videoUrl | String | La URL del vídeo. |
| videoEmbedCode | String | El código de inserción del vídeo. |
| thumbnailImageBytes | Byte[] | Los bytes de la imagen en miniatura. |
| width | Double | Ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100 %. |
| height | Double | Altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100 %. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones utilizando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

## Ejemplos

Muestra cómo insertar un vídeo en línea en un documento con una miniatura personalizada.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" ancho=\"640\" alto=\"360\" borde del marco=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // A continuación se muestran dos formas de crear una forma con una miniatura personalizada, que se vincula a un video en línea.
        // que se reproducirá cuando hagamos clic en la forma en Microsoft Word.
        // 1 - Insertar una forma en línea en el cursor de inserción del nodo del constructor:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - Insertar una forma flotante:
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
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, string, byte[], [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertonlinevideo_2}

Inserta un objeto de vídeo en línea en el documento y lo escala al tamaño especificado.

```csharp
public Shape InsertOnlineVideo(string videoUrl, string videoEmbedCode, byte[] thumbnailImageBytes, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    double width, double height, WrapType wrapType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| videoUrl | String | La URL del vídeo. |
| videoEmbedCode | String | El código de inserción del vídeo. |
| thumbnailImageBytes | Byte[] | Los bytes de la imagen en miniatura. |
| horzPos | RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| left | Double | Distancia en puntos desde el origen hasta el lado izquierdo de la imagen. |
| vertPos | RelativeVerticalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| top | Double | Distancia en puntos desde el origen hasta la parte superior de la imagen. |
| width | Double | Ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100 %. |
| height | Double | Altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100 %. |
| wrapType | WrapType | Especifica cómo ajustar el texto alrededor de la imagen. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones utilizando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

## Ejemplos

Muestra cómo insertar un vídeo en línea en un documento con una miniatura personalizada.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string videoUrl = "https://vimeo.com/52477838";
string videoEmbedCode =
    "<iframe src=\"https://player.vimeo.com/video/52477838\" ancho=\"640\" alto=\"360\" borde del marco=\"0\" " +
    "title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

byte[] thumbnailImageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(thumbnailImageBytes))
{
    using (Image image = Image.FromStream(stream))
    {
        // A continuación se muestran dos formas de crear una forma con una miniatura personalizada, que se vincula a un video en línea.
        // que se reproducirá cuando hagamos clic en la forma en Microsoft Word.
        // 1 - Insertar una forma en línea en el cursor de inserción del nodo del constructor:
        builder.InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image.Width, image.Height);

        builder.InsertBreak(BreakType.PageBreak);

        // 2 - Insertar una forma flotante:
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
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## InsertOnlineVideo(*string, double, double*) {#insertonlinevideo_1}

Inserta un objeto de vídeo en línea en el documento y lo escala al tamaño especificado.

```csharp
public Shape InsertOnlineVideo(string videoUrl, double width, double height)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| videoUrl | String | La URL del vídeo. |
| width | Double | Ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100 %. |
| height | Double | Altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100 %. |

### Valor_devuelto

El nodo de imagen que se acaba de insertar.

## Observaciones

Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones utilizando [`Shape`](../../../aspose.words.drawing/shape/) objeto devuelto por este método.

Se admite la inserción de vídeos en línea desde los siguientes recursos:

* https://www.youtube.com/
* https://vimeo.com/

Si su video en línea no se muestra correctamente, utilice`InsertOnlineVideo`, que acepta código HTML incrustado personalizado.

El código para insertar vídeo puede variar entre proveedores; consulte con su proveedor correspondiente para obtener más detalles.

## Ejemplos

Muestra cómo insertar un vídeo en línea en un documento usando una URL.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertOnlineVideo("https://youtu.be/g1N9ke8Prmk", 360, 270);

//Podemos ver el vídeo desde Microsoft Word haciendo clic en la forma.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertVideoWithUrl.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
