---
title: XpsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words for .NET
description: 使用 XpsSaveOptions UseBookFoldPrintingSettings 属性优化您的文档布局，实现无缝小册子打印以增强演示效果。
type: docs
weight: 50
url: /zh/net/aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings/
---
## XpsSaveOptions.UseBookFoldPrintingSettings property

获取或设置一个布尔值，指示是否应使用小册子打印布局保存文档，如果通过指定，则为 [`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/).

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## 评论

如果指定此选项，[`PageSet`](../../fixedpagesaveoptions/pageset/)保存时将被忽略。 此行为与 MS Word 匹配。 如果在页面设置中未指定书籍折叠打印设置，则此选项将不起作用。

## 例子

展示如何将文档以书本折叠的形式保存为 XPS 格式。

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// 创建一个“XpsSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .XPS 的方式。
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// 将“UseBookFoldPrintingSettings”属性设置为“true”来排列内容
// 以一种有助于我们使用它制作小册子的方式输出 XPS。
// 将“UseBookFoldPrintingSettings”属性设置为“false”以正常呈现 XPS。
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// 如果我们将文档渲染为小册子，则必须设置“MultiplePages”
// 将所有部分的页面设置对象的属性设置为“MultiplePagesType.BookFoldPrinting”。
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// 一旦我们打印了这份文件，我们就可以通过堆叠页面将其变成一本小册子
// 从打印机出来并向下折叠。
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### 也可以看看

* class [XpsSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
