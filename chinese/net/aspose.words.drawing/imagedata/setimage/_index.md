---
title: ImageData.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: 用于 .NET 的 Aspose.Words
description: ImageData SetImage 方法. 设置形状显示的图像 在 C#.
type: docs
weight: 200
url: /zh/net/aspose.words.drawing/imagedata/setimage/
---
## SetImage(*Image*) {#setimage}

设置形状显示的图像。

```csharp
public void SetImage(Image image)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| image | Image | 图像对象。 |

## 例子

演示如何在文档中显示本地文件系统中的图像。

```csharp
Document doc = new Document();

// 要在文档中显示图像，我们需要创建一个形状
// 其中将包含图像，然后将其附加到文档的正文中。
Shape imgShape;

// 下面是从本地文件系统中的文件获取图像的两种方法。
// 1 - 从图像文件创建图像对象：
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 - 使用流从本地文件系统打开图像文件：
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### 也可以看看

* class [ImageData](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)

---

## SetImage(*Stream*) {#setimage_1}

设置形状显示的图像。

```csharp
public void SetImage(Stream stream)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 包含图像的流。 |

## 例子

演示如何在文档中显示本地文件系统中的图像。

```csharp
Document doc = new Document();

// 要在文档中显示图像，我们需要创建一个形状
// 其中将包含图像，然后将其附加到文档的正文中。
Shape imgShape;

// 下面是从本地文件系统中的文件获取图像的两种方法。
// 1 - 从图像文件创建图像对象：
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 - 使用流从本地文件系统打开图像文件：
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### 也可以看看

* class [ImageData](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)

---

## SetImage(*string*) {#setimage_2}

设置形状显示的图像。

```csharp
public void SetImage(string fileName)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 图像文件。可以是文件名或 URL。 |

## 例子

演示如何将链接图像插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// 下面是将图像应用到形状以便其显示的两种方法。
// 1 - 设置形状以包含图像。
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// 我们存储在 shape 中的每个图像都会增加文档的大小。
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - 设置形状以链接到本地文件系统中的图像文件。
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// 链接到图像将节省空间并导致文档更小。
// 但是，文档只能正确显示图像
// 图像文件位于形状的“SourceFullName”属性指向的位置。
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### 也可以看看

* class [ImageData](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
