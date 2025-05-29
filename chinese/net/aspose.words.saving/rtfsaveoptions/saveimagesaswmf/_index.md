---
title: RtfSaveOptions.SaveImagesAsWmf
linktitle: SaveImagesAsWmf
articleTitle: SaveImagesAsWmf
second_title: Aspose.Words for .NET
description: 了解 RtfSaveOptions SaveImagesAsWmf 属性如何通过将所有图像保存为 WMF 来增强您的文档，从而实现卓越的质量和兼容性。
type: docs
weight: 50
url: /zh/net/aspose.words.saving/rtfsaveoptions/saveimagesaswmf/
---
## RtfSaveOptions.SaveImagesAsWmf property

当`真的`所有图像将保存为 WMF。

```csharp
public bool SaveImagesAsWmf { get; set; }
```

## 评论

此选项可能有助于避免写字板警告消息。

## 例子

展示如何在将文档保存为 RTF 时将文档中的所有图像转换为 Windows 图元文件格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg");

Assert.AreEqual(ImageType.Jpeg, imageShape.ImageData.ImageType);

builder.InsertParagraph();
builder.Writeln("Png image:");
imageShape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ImageType.Png, imageShape.ImageData.ImageType);

// 创建一个“RtfSaveOptions”对象传递给文档的“Save”方法来修改我们将其保存为 RTF 的方式。
RtfSaveOptions rtfSaveOptions = new RtfSaveOptions();

// 将“SaveImagesAsWmf”属性设置为“true”，以便在将文档保存为 RTF 时将文档中的所有图像转换为 WMF。
// 这样做将有助于写字板等阅读器阅读我们的文档。
// 将“SaveImagesAsWmf”属性设置为“false”以保留文档中所有图像的原始格式
// 将其保存为 RTF 格式。这将保留图像质量，但会牺牲与旧版 RTF 阅读器的兼容性。
rtfSaveOptions.SaveImagesAsWmf = saveImagesAsWmf;

doc.Save(ArtifactsDir + "RtfSaveOptions.SaveImagesAsWmf.rtf", rtfSaveOptions);

doc = new Document(ArtifactsDir + "RtfSaveOptions.SaveImagesAsWmf.rtf");

NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

if (saveImagesAsWmf)
{
    Assert.AreEqual(ImageType.Wmf, ((Shape)shapes[0]).ImageData.ImageType);
    Assert.AreEqual(ImageType.Wmf, ((Shape)shapes[1]).ImageData.ImageType);
}
else
{
    Assert.AreEqual(ImageType.Jpeg, ((Shape)shapes[0]).ImageData.ImageType);
    Assert.AreEqual(ImageType.Png, ((Shape)shapes[1]).ImageData.ImageType);
}
```

### 也可以看看

* class [RtfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
