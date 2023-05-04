---
title: ImageData.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words for .NET
description: ImageData SetImage method. Sets the image that the shape displays in C#.
type: docs
weight: 200
url: /net/aspose.words.drawing/imagedata/setimage/
---
## SetImage(*Image*) {#setimage}

Sets the image that the shape displays.

```csharp
public void SetImage(Image image)
```

| Parameter | Type | Description |
| --- | --- | --- |
| image | Image | The image object. |

## Examples

Shows how to display images from the local file system in a document.

```csharp
Document doc = new Document();

// To display an image in a document, we will need to create a shape
// which will contain an image, and then append it to the document's body.
Shape imgShape;

// Below are two ways of getting an image from a file in the local file system.
// 1 -  Create an image object from an image file:
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 -  Open an image file from the local file system using a stream:
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### See Also

* class [ImageData](../)
* namespace [Aspose.Words.Drawing](../../imagedata/)
* assembly [Aspose.Words](../../../)

---

## SetImage(*Stream*) {#setimage_1}

Sets the image that the shape displays.

```csharp
public void SetImage(Stream stream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | The stream that contains the image. |

## Examples

Shows how to display images from the local file system in a document.

```csharp
Document doc = new Document();

// To display an image in a document, we will need to create a shape
// which will contain an image, and then append it to the document's body.
Shape imgShape;

// Below are two ways of getting an image from a file in the local file system.
// 1 -  Create an image object from an image file:
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 -  Open an image file from the local file system using a stream:
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### See Also

* class [ImageData](../)
* namespace [Aspose.Words.Drawing](../../imagedata/)
* assembly [Aspose.Words](../../../)

---

## SetImage(*string*) {#setimage_2}

Sets the image that the shape displays.

```csharp
public void SetImage(string fileName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The image file. Can be a file name or a URL. |

## Examples

Shows how to insert a linked image into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Below are two ways of applying an image to a shape so that it can display it.
// 1 -  Set the shape to contain the image.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Every image that we store in shape will increase the size of our document.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 -  Set the shape to link to an image file in the local file system.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Linking to images will save space and result in a smaller document.
// However, the document can only display the image correctly while
// the image file is present at the location that the shape's "SourceFullName" property points to.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### See Also

* class [ImageData](../)
* namespace [Aspose.Words.Drawing](../../imagedata/)
* assembly [Aspose.Words](../../../)
