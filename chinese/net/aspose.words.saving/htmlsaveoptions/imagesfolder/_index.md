---
title: HtmlSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words for .NET
description: 探索 HtmlSaveOptions ImagesFolder 属性。轻松设置将文档导出为 HTML 时用于保存图像的文件夹。立即简化您的工作流程！
type: docs
weight: 360
url: /zh/net/aspose.words.saving/htmlsaveoptions/imagesfolder/
---
## HtmlSaveOptions.ImagesFolder property

指定将文档导出为 HTML 格式时保存图像的物理文件夹。 默认值为空字符串。

```csharp
public string ImagesFolder { get; set; }
```

## 评论

当你保存[`Document`](../../../aspose.words/document/)在 HTML 格式中，Aspose.Words 需要将文档中嵌入的所有 图像保存为独立文件。`ImagesFolder` 允许您指定图像的保存位置，并且[`ImagesFolderAlias`](../imagesfolderalias/) 允许指定如何构建图像 URI。

如果您将文档保存到文件中并提供文件名，Aspose.Words 默认会将 图像保存在文档文件所在的文件夹中。使用`ImagesFolder` 来覆盖此行为。

如果您将文档保存到流中，Aspose.Words 没有用于保存图像的文件夹 ，但仍需要将图像保存在某个位置。在这种情况下，您需要在`ImagesFolder`属性或提供自定义流 via [`ImageSavingCallback`](../imagesavingcallback/)事件处理程序。

如果指定的文件夹`ImagesFolder`不存在，将自动创建。

[`ResourceFolder`](../resourcefolder/)是指定保存图像的文件夹的另一种方法。

## 例子

展示如何在保存为 .html 后指定存储链接图像的文件夹。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// 设置一个选项，将表单字段导出为纯文本而不是 HTML 输入元素。
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
