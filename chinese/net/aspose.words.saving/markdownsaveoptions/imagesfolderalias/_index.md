---
title: MarkdownSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words for .NET
description: 探索 MarkdownSaveOptions ImagesFolderAlias 属性，轻松管理文档中的图像 URI。这项重要功能将简化您的工作流程！
type: docs
weight: 90
url: /zh/net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

指定用于构建写入文档的图像 URI 的文件夹的名称。 默认值为空字符串。

```csharp
public string ImagesFolderAlias { get; set; }
```

## 评论

当你保存[`Document`](../../../aspose.words/document/)在Markdown格式， Aspose.Words 需要将文档中嵌入的所有图像保存为独立文件。 [`ImagesFolder`](../imagesfolder/)允许您指定图像的保存位置和 `ImagesFolderAlias`允许指定如何构建图像 URI。

如果`ImagesFolderAlias`不是空字符串，那么 Markdown 中的图片 URI written 将是ImagesFolderAlias + &lt;图像文件名&gt;。

如果`ImagesFolderAlias`是空字符串，则 Markdown 中的图像 URI written 将是ImagesFolder + &lt;图像文件名&gt;。

如果`ImagesFolderAlias`设置为 '.'（点），则无论其他选项如何，图像文件 name 都将不带路径地写入 Markdown。

## 例子

展示如何指定用于构建图像 URI 的文件夹的名称。

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
builder.InsertImage(ImageDir + "Logo.jpg");

string imagesFolder = Path.Combine(ArtifactsDir, "ImagesDir");
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// 使用“ImagesFolder”属性在本地文件系统中分配一个文件夹，
// Aspose.Words 将保存文档的所有链接图像。
saveOptions.ImagesFolder = imagesFolder;
// 使用“ImagesFolderAlias”属性来使用此文件夹
// 构建图像 URI 时，而不是图像文件夹的名称。
saveOptions.ImagesFolderAlias = "http://example.com/images”;

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### 也可以看看

* class [MarkdownSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
