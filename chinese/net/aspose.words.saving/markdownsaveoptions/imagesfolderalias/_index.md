---
title: MarkdownSaveOptions.ImagesFolderAlias
second_title: Aspose.Words for .NET API 参考
description: MarkdownSaveOptions 财产. 指定用于构建写入文档的图像 URI 的文件夹名称 默认为空字符串
type: docs
weight: 50
url: /zh/net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

指定用于构建写入文档的图像 URI 的文件夹名称。 默认为空字符串。

```csharp
public string ImagesFolderAlias { get; set; }
```

### 评论

当您保存一个[`Document`](../../../aspose.words/document/)在Markdown格式, Aspose.Words 需要将文档中嵌入的所有图像保存为独立文件。 [`ImagesFolder`](../imagesfolder/)允许您指定图像的保存位置 and `ImagesFolderAlias`允许指定如何构造图像 URI。

如果`ImagesFolderAlias`不是空字符串，那么 Markdown 中写入的图像 URI 将为ImagesFolderAlias + &lt;图像文件名&gt;。

如果`ImagesFolderAlias`是一个空字符串，那么 Markdown 中写入的图像 URI 将是ImagesFolder + &lt;图像文件名&gt;。

如果`ImagesFolderAlias`被设定为 '。' （点），那么无论其他选项如何，图像文件名 都将被写入Markdown，不带路径。

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


