---
title: DocumentBuilder.InsertNode
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentBuilder método. Inserta un nodo de nivel de texto dentro del párrafo actual antes del cursor.
type: docs
weight: 360
url: /es/net/aspose.words/documentbuilder/insertnode/
---
## DocumentBuilder.InsertNode method

Inserta un nodo de nivel de texto dentro del párrafo actual antes del cursor.

```csharp
public void InsertNode(Node node)
```

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

* class [Node](../../node/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)


