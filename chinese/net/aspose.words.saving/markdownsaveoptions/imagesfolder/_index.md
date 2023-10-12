---
title: MarkdownSaveOptions.ImagesFolder
second_title: Aspose.Words for .NET API 参考
description: MarkdownSaveOptions 财产. 指定将文档导出到 时保存图像的物理文件夹Markdown格式默认为空字符串
type: docs
weight: 40
url: /zh/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

指定将文档导出到 时保存图像的物理文件夹Markdown格式。默认为空字符串。

```csharp
public string ImagesFolder { get; set; }
```

### 评论

当您保存[`Document`](../../../aspose.words/document/)在Markdown格式, Aspose.Words 需要将文档中嵌入的所有图像保存为独立文件。 `ImagesFolder`允许您指定图像的保存位置。

如果将文档保存到文件中并提供文件名，默认情况下，Aspose.Words 会将图像保存在 与保存文档文件的同一文件夹中。使用`ImagesFolder`覆盖此行为。

如果将文档保存到流中，Aspose.Words 没有文件夹 来保存图像，但仍然需要将图像保存在某个地方。在这种情况下， 您需要在`ImagesFolder`属性.

如果指定的文件夹`ImagesFolder`不存在，将自动创建。

### 例子

演示如何指定用于构造图像 URI 的文件夹的名称。

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
Image image = Image.FromFile(ImageDir + "Logo.jpg");
builder.InsertImage(image);

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// 使用“ImagesFolder”属性在本地文件系统中分配一个文件夹
// Aspose.Words 将保存文档的所有链接图像。
saveOptions.ImagesFolder = ArtifactsDir + "ImagesDir/";
// 使用“ImagesFolderAlias”属性来使用此文件夹
// 当构造图像 URI 而不是图像文件夹的名称时。
saveOptions.ImagesFolderAlias = "http://example.com/images";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

演示如何指定用于构造图像 URI (.NetStandard 2.0) 的文件夹的名称。

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
    builder.InsertImage(bitmap);

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// 使用“ImagesFolder”属性在本地文件系统中分配一个文件夹
// Aspose.Words 将保存文档的所有链接图像。
saveOptions.ImagesFolder = ArtifactsDir + "ImagesDir/";
// 使用“ImagesFolderAlias”属性来使用此文件夹
// 当构造图像 URI 而不是图像文件夹的名称时。
saveOptions.ImagesFolderAlias = "http://example.com/images";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### 也可以看看

* class [MarkdownSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../markdownsaveoptions/)
* 部件 [Aspose.Words](../../../)


