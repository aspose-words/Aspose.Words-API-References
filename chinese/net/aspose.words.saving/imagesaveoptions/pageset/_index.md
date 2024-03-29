---
title: ImageSaveOptions.PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: 用于 .NET 的 Aspose.Words
description: ImageSaveOptions PageSet 财产. 获取或设置要呈现的页面 默认为文档中的所有页面 在 C#.
type: docs
weight: 100
url: /zh/net/aspose.words.saving/imagesaveoptions/pageset/
---
## ImageSaveOptions.PageSet property

获取或设置要呈现的页面。 默认为文档中的所有页面。

```csharp
public PageSet PageSet { get; set; }
```

## 评论

该属性仅在渲染文档页面时有效。将形状渲染到图像时会忽略此属性。

## 例子

展示如何根据确切的页面范围提取页面。

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

演示如何指定文档中的哪一页呈现为图像。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world! This is page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("This is page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("This is page 3.");

Assert.AreEqual(3, doc.PageCount);

// 当我们将文档保存为图像时，Aspose.Words 默认只渲染第一页。
// 我们可以传递一个 SaveOptions 对象来指定要渲染的不同页面。
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Gif);

// 将文档的每一页渲染为单独的图像文件。
for (int i = 1; i <= doc.PageCount; i++)
{
    saveOptions.PageSet = new PageSet(1);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageIndex.Page {i}.gif", saveOptions);
}
```

演示如何将文档的每一页渲染为单独的 TIFF 图像。

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
    // 从哪个开始渲染文档。
    options.PageSet = new PageSet(i);
    // 以 2325x5325 像素和 600 dpi 导出页面。
    options.Resolution = 600;
    options.ImageSize = new Size(2325, 5325);

    doc.Save(ArtifactsDir + $"ImageSaveOptions.PageByPage.{i + 1}.tiff", options);
}
```

演示如何将文档中的一页渲染为 JPEG 图像。

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
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);

// 将“PageSet”设置为“1”以通过以下方式选择第二页
// 开始渲染文档的从零开始的索引。
options.PageSet = new PageSet(1);

// 当我们将文档保存为 JPEG 格式时，Aspose.Words 只渲染一页。
// 该图像将包含从第二页开始的一页，
// 这只是原始文档的第二页。
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### 也可以看看

* class [PageSet](../../pageset/)
* class [ImageSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
