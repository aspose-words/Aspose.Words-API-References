---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
linktitle: OpenHyperlinksInNewWindow
articleTitle: OpenHyperlinksInNewWindow
second_title: Aspose.Words for .NET
description: 使用 PdfSaveOptions 控制 PDF 中的超链接行为。轻松设置链接在新窗口或标签页中打开，提升用户体验。
type: docs
weight: 230
url: /zh/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

获取或设置一个值，确定输出 PDF 文档中的超链接是否强制在浏览器的新窗口（或选项卡）中打开。

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

## 评论

默认值为`错误的` 。当此值设置为`真的` 超链接使用 JavaScript 代码保存。 JavaScript 代码是`app.launchURL(“URL”，true);`, 其中`网址`是一个超链接。

请注意，如果此选项设置为`真的`超链接在某些 PDF 阅读器（例如 Chrome、Firefox）中不起作用 。

PDF/A-1 和 PDF/A-2 合规性禁止 JavaScript 操作。`错误的`当 保存为 PDF/A-1 和 PDF/A-2 时将自动使用。

## 例子

展示如何在我们转换为 PDF 的文档中保存超链接，以便我们单击它们时打开新页面。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose", false);

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 将“OpenHyperlinksInNewWindow”属性设置为“true”，以使用 Javascript 代码保存所有超链接
// 强制读者在新窗口/浏览器选项卡中打开这些链接。
// 将“OpenHyperlinksInNewWindow”属性设置为“false”以正常保存所有超链接。
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
