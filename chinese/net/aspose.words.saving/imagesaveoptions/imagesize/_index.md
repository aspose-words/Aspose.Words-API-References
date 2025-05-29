---
title: ImageSaveOptions.ImageSize
linktitle: ImageSize
articleTitle: ImageSize
second_title: Aspose.Words for .NET
description: 探索 ImageSaveOptions 的 ImageSize 属性，轻松管理和自定义图像尺寸（以像素为单位），以获得最佳效果。
type: docs
weight: 70
url: /zh/net/aspose.words.saving/imagesaveoptions/imagesize/
---
## ImageSaveOptions.ImageSize property

获取或设置生成的图像的大小（以像素为单位）。

```csharp
public Size ImageSize { get; set; }
```

## 评论

此属性仅在保存为光栅图像格式时有效。

默认值为 (0 x 0)，这意味着生成的图像的大小将根据图像的点数、指定的分辨率和比例来计算 。

## 例子

展示如何将文档的每一页渲染为单独的 TIFF 图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// 创建一个“ImageSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档呈现为图像的方式。
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

for (int i = 0; i < doc.PageCount; i++)
{
    // 将“PageSet”属性设置为第一页的页码
    // 从哪里开始渲染文档。
    options.PageSet = new PageSet(i);
    // 以 2325x5325 像素和 600 dpi 导出页面。
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

### 也可以看看

* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
