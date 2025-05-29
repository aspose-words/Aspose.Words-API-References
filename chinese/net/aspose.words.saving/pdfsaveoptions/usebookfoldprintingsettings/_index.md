---
title: PdfSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words for .NET
description: 发现 PdfSaveOptions UseBookFoldPrintingSettings 属性可以轻松地将文档保存在小册子布局中，从而提高打印效率。
type: docs
weight: 320
url: /zh/net/aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/
---
## PdfSaveOptions.UseBookFoldPrintingSettings property

获取或设置一个布尔值，指示是否应使用小册子打印布局保存文档，如果通过指定，则为 [`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/).

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## 评论

如果指定此选项，[`PageSet`](../../fixedpagesaveoptions/pageset/)保存时将被忽略。 此行为与 MS Word 匹配。 如果在页面设置中未指定书籍折叠打印设置，则此选项将不起作用。

## 例子

展示如何将文档以书本折叠的形式保存为 PDF 格式。

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 将“UseBookFoldPrintingSettings”属性设置为“true”来排列内容
// 以帮助我们使用它来制作小册子的方式输出 PDF。
// 将“UseBookFoldPrintingSettings”属性设置为“false”以正常呈现 PDF。
options.UseBookFoldPrintingSettings = renderTextAsBookfold;

// 如果我们将文档渲染为小册子，则必须设置“MultiplePages”
// 将所有部分的页面设置对象的属性设置为“MultiplePagesType.BookFoldPrinting”。
if (renderTextAsBookfold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// 一旦我们在页面的两面打印了这份文件，我们就可以一次性将所有页面向中间折叠，
// 并且内容将以创建小册子的方式排列。
doc.Save(ArtifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
