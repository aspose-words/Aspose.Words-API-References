---
title: PdfSaveOptions.UseBookFoldPrintingSettings
second_title: Aspose.Words for .NET API 参考
description: PdfSaveOptions 财产. 获取或设置一个布尔值指示是否应使用小册子打印布局保存文档 如果通过指定MultiplePages.
type: docs
weight: 300
url: /zh/net/aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/
---
## PdfSaveOptions.UseBookFoldPrintingSettings property

获取或设置一个布尔值，指示是否应使用小册子打印布局保存文档， 如果通过指定[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/).

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

### 评论

如果指定此选项，[`PageSet`](../../fixedpagesaveoptions/pageset/)保存时被忽略。 此行为与 MS Word 匹配。 如果页面设置中未指定书籍折叠打印设置，则此选项将不起作用。

### 例子

演示如何以书籍折叠的形式将文档保存为 PDF 格式。

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions options = new PdfSaveOptions();

// 将“UseBookFoldPrintingSettings”属性设置为“true”以排列内容
// 在输出 PDF 中以帮助我们使用它制作小册子的方式。
// 将“UseBookFoldPrintingSettings”属性设置为“false”以正常渲染 PDF。
options.UseBookFoldPrintingSettings = renderTextAsBookfold;

// 如果我们将文档呈现为小册子，则必须设置“MultiplePages”
// 所有部分的页面设置对象的属性为“MultiplePagesType.BookFoldPrinting”。
if (renderTextAsBookfold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// 一旦我们在页面的两面打印该文档，我们就可以立即将所有页面从中间折叠起来，
// 内容将以创建小册子的方式排列。
doc.Save(ArtifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### 也可以看看

* class [PdfSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../pdfsaveoptions/)
* 部件 [Aspose.Words](../../../)


