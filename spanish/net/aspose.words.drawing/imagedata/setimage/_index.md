---
title: SetImage
second_title: Referencia de API de Aspose.Words para .NET
description: Establece la imagen que muestra la forma.
type: docs
weight: 200
url: /es/net/aspose.words.drawing/imagedata/setimage/
---
## SetImage(Image) {#setimage}

Establece la imagen que muestra la forma.

```csharp
public void SetImage(Image image)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| image | Image | El objeto de la imagen. |

### Ejemplos

Muestra cómo mostrar imágenes del sistema de archivos local en un documento.

```csharp
Document doc = new Document();

// Para mostrar una imagen en un documento, necesitaremos crear una forma
// que contendrá una imagen y luego la agregará al cuerpo del documento.
Shape imgShape;

// A continuación se muestran dos formas de obtener una imagen de un archivo en el sistema de archivos local.
// 1 - Crear un objeto de imagen a partir de un archivo de imagen:
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 - Abra un archivo de imagen desde el sistema de archivos local usando una secuencia:
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### Ver también

* class [ImageData](../)
* espacio de nombres [Aspose.Words.Drawing](../../imagedata/)
* asamblea [Aspose.Words](../../../)

---

## SetImage(Stream) {#setimage_1}

Establece la imagen que muestra la forma.

```csharp
public void SetImage(Stream stream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | El flujo que contiene la imagen. |

### Ejemplos

Muestra cómo mostrar imágenes del sistema de archivos local en un documento.

```csharp
Document doc = new Document();

// Para mostrar una imagen en un documento, necesitaremos crear una forma
// que contendrá una imagen y luego la agregará al cuerpo del documento.
Shape imgShape;

// A continuación se muestran dos formas de obtener una imagen de un archivo en el sistema de archivos local.
// 1 - Crear un objeto de imagen a partir de un archivo de imagen:
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 - Abra un archivo de imagen desde el sistema de archivos local usando una secuencia:
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### Ver también

* class [ImageData](../)
* espacio de nombres [Aspose.Words.Drawing](../../imagedata/)
* asamblea [Aspose.Words](../../../)

---

## SetImage(string) {#setimage_2}

Establece la imagen que muestra la forma.

```csharp
public void SetImage(string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | El archivo de imagen. Puede ser un nombre de archivo o una URL. |

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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
