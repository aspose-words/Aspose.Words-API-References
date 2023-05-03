---
title: ImageData.SourceFullName
linktitle: SourceFullName
second_title: Aspose.Words for .NET API Reference
description: ImageData SourceFullName property. Gets or sets the path and name of the source file for the linked image in C#.
type: docs
weight: 170
url: /net/aspose.words.drawing/imagedata/sourcefullname/
---
## ImageData.SourceFullName property

Gets or sets the path and name of the source file for the linked image.

```csharp
public string SourceFullName { get; set; }
```

## Remarks

The default value is an empty string.

If `SourceFullName` is not an empty string, the image is linked.

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
