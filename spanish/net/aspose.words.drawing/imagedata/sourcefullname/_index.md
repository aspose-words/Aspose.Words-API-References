---
title: ImageData.SourceFullName
second_title: Referencia de API de Aspose.Words para .NET
description: ImageData propiedad. Obtiene o establece la ruta y el nombre del archivo de origen de la imagen vinculada.
type: docs
weight: 170
url: /es/net/aspose.words.drawing/imagedata/sourcefullname/
---
## ImageData.SourceFullName property

Obtiene o establece la ruta y el nombre del archivo de origen de la imagen vinculada.

```csharp
public string SourceFullName { get; set; }
```

### Observaciones

El valor predeterminado es una cadena vacía.

Si`SourceFullName` no es una cadena vacía, la imagen está vinculada.

### Ejemplos

Muestra cómo insertar una imagen vinculada en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// A continuación hay dos formas de aplicar una imagen a una forma para que pueda mostrarla.
// 1 - Establecer la forma para contener la imagen.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Cada imagen que almacenemos en forma aumentará el tamaño de nuestro documento.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Configure la forma para que se vincule a un archivo de imagen en el sistema de archivos local.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Vincular imágenes ahorrará espacio y dará como resultado un documento más pequeño.
// Sin embargo, el documento solo puede mostrar la imagen correctamente mientras
// el archivo de imagen está presente en la ubicación a la que apunta la propiedad "SourceFullName" de la forma.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Ver también

* class [ImageData](../)
* espacio de nombres [Aspose.Words.Drawing](../../imagedata/)
* asamblea [Aspose.Words](../../../)


