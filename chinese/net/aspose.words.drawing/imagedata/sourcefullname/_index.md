---
title: ImageData.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words for .NET
description: 发现 ImageData SourceFullName 属性可以轻松管理链接的图像路径和文件名，从而提高图像处理效率。
type: docs
weight: 170
url: /zh/net/aspose.words.drawing/imagedata/sourcefullname/
---
## ImageData.SourceFullName property

获取或设置链接图像的源文件的路径和名称。

```csharp
public string SourceFullName { get; set; }
```

## 评论

默认值为空字符串。

如果`SourceFullName`不是空字符串，图像已链接。

## 例子

展示如何将链接图像插入文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// 以下是将图像应用到形状以便显示它的两种方法。
// 1 - 设置形状以包含图像。
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// 我们存储在形状中的每个图像都会增加文档的大小。
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - 设置形状以链接到本地文件系统中的图像文件。
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// 链接到图像将节省空间并产生更小的文档。
// 但是，文档只能在
// 图像文件位于形状的“SourceFullName”属性指向的位置。
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### 也可以看看

* class [ImageData](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
