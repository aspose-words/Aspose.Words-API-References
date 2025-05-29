---
title: XpsSaveOptions
linktitle: XpsSaveOptions
articleTitle: XpsSaveOptions
second_title: Aspose.Words for .NET
description: 探索 XpsSaveOptions 构造函数，轻松创建以 XPS 格式保存文档的实例，提高文档管理效率。
type: docs
weight: 10
url: /zh/net/aspose.words.saving/xpssaveoptions/xpssaveoptions/
---
## XpsSaveOptions() {#constructor}

初始化此类的新实例，可用于保存 document 在Xps格式.

```csharp
public XpsSaveOptions()
```

## 例子

展示如何限制已保存 XPS 文档大纲中出现的标题级别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入可作为 1、2 和 3 级目录条目的标题。
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// 创建一个“XpsSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .XPS 的方式。
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// 输出的 XPS 文档将包含一个大纲，即列出文档正文中标题的目录。
// 单击此大纲中的条目将带我们到其相应标题的位置。
// 将“HeadingsOutlineLevels”属性设置为“2”，以从大纲中排除所有级别高于 2 的标题。
// 我们上面插入的最后两个标题将不会出现。
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### 也可以看看

* class [XpsSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)

---

## XpsSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

初始化此类的新实例，可用于保存 document 在Xps或者OpenXps格式.

```csharp
public XpsSaveOptions(SaveFormat saveFormat)
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XpsSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
