---
title: Shape.ImageData
second_title: Referencia de API de Aspose.Words para .NET
description: Shape propiedad. Proporciona acceso a la imagen de la forma. Devuelvenulo si la forma no puede tener una imagen.
type: docs
weight: 110
url: /es/net/aspose.words.drawing/shape/imagedata/
---
## Shape.ImageData property

Proporciona acceso a la imagen de la forma. Devuelve`nulo` si la forma no puede tener una imagen.

```csharp
public ImageData ImageData { get; }
```

### Ejemplos

Muestra cómo extraer imágenes de un documento y guardarlas en el sistema de archivos local como archivos individuales.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Obtener la colección de formas del documento,
// y guarda los datos de la imagen de cada forma con una imagen como un archivo en el sistema de archivos local.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Los datos de imagen de las formas pueden contener imágenes de muchos formatos de imagen posibles.
        // Podemos determinar una extensión de archivo para cada imagen automáticamente, según su formato.
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
// 1 - Establece la forma para contener la imagen.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Cada imagen que almacenemos en forma aumentará el tamaño de nuestro documento.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Establece la forma para vincular a un archivo de imagen en el sistema de archivos local.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Vincular a imágenes ahorrará espacio y dará como resultado un documento más pequeño.
// Sin embargo, el documento sólo puede mostrar la imagen correctamente mientras
// el archivo de imagen está presente en la ubicación a la que apunta la propiedad "SourceFullName" de la forma.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Ver también

* class [ImageData](../../imagedata/)
* class [Shape](../)
* espacio de nombres [Aspose.Words.Drawing](../../shape/)
* asamblea [Aspose.Words](../../../)


