---
title: ImageData Class
linktitle: ImageData
articleTitle: ImageData
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Drawing.ImageData su solución para definir y gestionar imágenes en formas. ¡Mejore el diseño de sus documentos sin esfuerzo!
type: docs
weight: 1390
url: /es/net/aspose.words.drawing/imagedata/
---
## ImageData class

Define una imagen para una forma.

Para obtener más información, visite el[Trabajar con imágenes](https://docs.aspose.com/words/net/working-with-images/) Artículo de documentación.

```csharp
public class ImageData
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel/) { get; set; } | Determina si una imagen se mostrará en blanco y negro. |
| [Borders](../../aspose.words.drawing/imagedata/borders/) { get; } | Obtiene la colección de bordes de la imagen. Los bordes solo tienen efecto en imágenes en línea. |
| [Brightness](../../aspose.words.drawing/imagedata/brightness/) { get; set; } | Obtiene o establece el brillo de la imagen. El valor de esta propiedad debe ser un número entre 0.0 (más tenue) y 1.0 (más brillante). |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey/) { get; set; } | Define el valor de color de la imagen que se tratará como transparente. |
| [Contrast](../../aspose.words.drawing/imagedata/contrast/) { get; set; } | Obtiene o establece el contraste de la imagen especificada. El valor de esta propiedad debe ser un número entre 0.0 (el menor contraste) y 1.0 (el mayor contraste). |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom/) { get; set; } | Define la fracción de eliminación de la imagen del lado inferior. |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft/) { get; set; } | Define la fracción de eliminación de imagen del lado izquierdo. |
| [CropRight](../../aspose.words.drawing/imagedata/cropright/) { get; set; } | Define la fracción de eliminación de imagen del lado derecho. |
| [CropTop](../../aspose.words.drawing/imagedata/croptop/) { get; set; } | Define la fracción de eliminación de la imagen desde el lado superior. |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale/) { get; set; } | Determina si una imagen se mostrará en modo de escala de grises. |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage/) { get; } | Devuelve`verdadero` si la forma tiene bytes de imagen o vincula una imagen. |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes/) { get; set; } | Obtiene o establece los bytes sin procesar de la imagen almacenada en la forma. |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize/) { get; } | Obtiene la información sobre el tamaño y la resolución de la imagen. |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype/) { get; } | Obtiene el tipo de imagen. |
| [IsLink](../../aspose.words.drawing/imagedata/islink/) { get; } | Devuelve`verdadero` si la imagen está vinculada a la forma (cuando[`SourceFullName`](./sourcefullname/) se especifica). |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly/) { get; } | Devuelve`verdadero` Si la imagen está vinculada y no almacenada en el documento. |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname/) { get; set; } | Obtiene o establece la ruta y el nombre del archivo de origen de la imagen vinculada. |
| [Title](../../aspose.words.drawing/imagedata/title/) { get; set; } | Define el título de una imagen. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [FitImageToShape](../../aspose.words.drawing/imagedata/fitimagetoshape/)() | Ajusta los datos de la imagen al marco de forma para que la relación de aspecto de los datos de la imagen coincida con la relación de aspecto del marco de forma. |
| [Save](../../aspose.words.drawing/imagedata/save/#save)(*Stream*) | Guarda la imagen en la secuencia especificada. |
| [Save](../../aspose.words.drawing/imagedata/save/#save_1)(*string*) | Guarda la imagen en un archivo. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage)(*Image*) | Establece la imagen que muestra la forma. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_1)(*Stream*) | Establece la imagen que muestra la forma. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_2)(*string*) | Establece la imagen que muestra la forma. |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray/)() | Devuelve bytes de imagen para cualquier imagen, independientemente de si la imagen está almacenada o vinculada. |
| [ToImage](../../aspose.words.drawing/imagedata/toimage/)() | Obtiene la imagen almacenada en la forma como unaImage objeto. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream/)() | Crea y devuelve una secuencia que contiene los bytes de la imagen. |

## Observaciones

Utilice el[`ImageData`](../shape/imagedata/)propiedad para acceder y modificar la imagen dentro de una forma. No crea instancias de la`ImageData` clase directamente.

Una imagen puede almacenarse dentro de una forma, vincularse a un archivo externo o ambos (vincularse y almacenarse en el documento).

Independientemente de si la imagen está almacenada dentro de la forma o vinculada, siempre puede acceder a la imagen actual usando el[`ToByteArray`](./tobytearray/) ,[`ToStream`](./tostream/) ,[`ToImage`](./toimage/) o[`Save`](./save/) métodos. Si la imagen está almacenada dentro de la forma, también puedes acceder a ella directamente usando el[`ImageBytes`](./imagebytes/) propiedad.

Para almacenar una imagen dentro de una forma, utilice el[`SetImage`](./setimage/) método. Para vincular una imagen a una forma, configure el[`SourceFullName`](./sourcefullname/) propiedad.

## Ejemplos

Muestra cómo extraer imágenes de un documento y guardarlas en el sistema de archivos local como archivos individuales.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Obtener la colección de formas del documento,
// y guarde los datos de imagen de cada forma con una imagen como un archivo en el sistema de archivos local.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Los datos de imagen de las formas pueden contener imágenes de muchos formatos de imagen posibles.
        //Podemos determinar automáticamente una extensión de archivo para cada imagen, en función de su formato.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Muestra cómo insertar una imagen vinculada en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// A continuación se muestran dos formas de aplicar una imagen a una forma para que pueda mostrarla.
// 1 - Establece la forma que contendrá la imagen.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

//Cada imagen que almacenemos en shape aumentará el tamaño de nuestro documento.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Establece la forma para vincularla a un archivo de imagen en el sistema de archivos local.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Vincular a las imágenes ahorrará espacio y dará como resultado un documento más pequeño.
// Sin embargo, el documento sólo puede mostrar la imagen correctamente mientras
// el archivo de imagen está presente en la ubicación a la que apunta la propiedad "SourceFullName" de la forma.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
