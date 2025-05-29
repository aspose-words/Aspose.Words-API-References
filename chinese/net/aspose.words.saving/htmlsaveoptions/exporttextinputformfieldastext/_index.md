---
title: HtmlSaveOptions.ExportTextInputFormFieldAsText
linktitle: ExportTextInputFormFieldAsText
articleTitle: ExportTextInputFormFieldAsText
second_title: Aspose.Words for .NET
description: 了解 HtmlSaveOptions ExportTextInputFormFieldAsText 属性如何优化文本输入表单字段，实现无缝 HTML 或 MHTML 保存。增强您的导出流程！
type: docs
weight: 260
url: /zh/net/aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/
---
## HtmlSaveOptions.ExportTextInputFormFieldAsText property

控制如何将文本输入表单字段保存为 HTML 或 MHTML。 默认值为`错误的`.

```csharp
public bool ExportTextInputFormFieldAsText { get; set; }
```

## 评论

当设置为`真的`，将文本输入表单字段导出为普通文本。 当`错误的`，将 Word 文本输入表单字段导出为 HTML 中的 INPUT 元素。

导出为 EPUB 时，文本输入表单字段始终保存为文本，以满足此格式的要求。

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
