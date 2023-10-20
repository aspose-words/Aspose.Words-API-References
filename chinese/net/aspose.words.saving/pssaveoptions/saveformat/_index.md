---
title: PsSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: 用于 .NET 的 Aspose.Words
description: PsSaveOptions SaveFormat 财产. 指定使用此保存选项对象时保存文档的格式 只能是Ps 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.saving/pssaveoptions/saveformat/
---
## PsSaveOptions.SaveFormat property

指定使用此保存选项对象时保存文档的格式。 只能是Ps.

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## 例子

演示如何以书籍折叠的形式将文档保存为 Postscript 格式。

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// 创建一个“PsSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 PostScript 的方式。
// 将“UseBookFoldPrintingSettings”属性设置为“true”以排列内容
// 在输出的 Postscript 文档中以帮助我们制作小册子的方式。
// 将“UseBookFoldPrintingSettings”属性设置为“false”以正常保存文档。
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// 如果我们将文档呈现为小册子，则必须设置“MultiplePages”
// 所有部分的页面设置对象的属性为“MultiplePagesType.BookFoldPrinting”。
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// 一旦我们在页面的两面打印该文档，我们就可以立即将所有页面从中间折叠起来，
// 内容将以创建小册子的方式排列。
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### 也可以看看

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PsSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
