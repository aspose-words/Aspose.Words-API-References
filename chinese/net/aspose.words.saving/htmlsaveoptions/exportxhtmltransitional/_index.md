---
title: HtmlSaveOptions.ExportXhtmlTransitional
linktitle: ExportXhtmlTransitional
articleTitle: ExportXhtmlTransitional
second_title: Aspose.Words for .NET
description: 使用 HtmlSaveOptions ExportXhtmlTransitional 属性优化您的 HTML。控制 DOCTYPE 声明，以提高与 HTML、MHTML 和 EPUB 格式的兼容性。
type: docs
weight: 280
url: /zh/net/aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/
---
## HtmlSaveOptions.ExportXhtmlTransitional property

指定在保存为 HTML 或 MHTML 时是否写入 DOCTYPE 声明。 当`真的`，在文档的根元素之前写入 DOCTYPE 声明。 默认值为`错误的`. 保存为 EPUB 或 HTML5 时（Html5 ) DOCTYPE 声明总是写成.

```csharp
public bool ExportXhtmlTransitional { get; set; }
```

## 评论

无论此设置如何，Aspose.Words 总是会编写格式良好的 HTML。

什么时候`真的`，HTML 输出文档的开头将如下所示：

Aspose.Words 旨在根据 XHTML 1.0 Transitional 规范输出 XHTML，但输出结果并不总是符合 DTD 的验证。Microsoft Word 文档中的某些结构很难或无法映射到符合 XHTML 模式的文档。例如，XHTML 不允许嵌套列表（UL 元素不能嵌套在另一个 UL 元素中），但在 Microsoft Word 文档中，多级列表却经常出现。

```csharp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
<!DOCTYPE html
      PUBLIC "-//W3C//DTD XHTML 1.0 过渡//EN”
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
```

## 例子

展示在将文档转换为 Xhtml 1.0 过渡标准时如何显示 DOCTYPE 标题。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = HtmlVersion.Xhtml,
    ExportXhtmlTransitional = showDoctypeDeclaration,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// 如果我们将“ExportXhtmlTransitional”标志设置为“true”，我们的文档将仅包含 DOCTYPE 声明标题。
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html");
string newLine = Environment.NewLine;

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        $"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>{newLine}" +
        $"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">{newLine}" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
else
    Assert.True(outDocContents.Contains("<html>"));
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
