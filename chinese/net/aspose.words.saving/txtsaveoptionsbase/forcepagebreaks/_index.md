---
title: TxtSaveOptionsBase.ForcePageBreaks
linktitle: ForcePageBreaks
articleTitle: ForcePageBreaks
second_title: 用于 .NET 的 Aspose.Words
description: TxtSaveOptionsBase ForcePageBreaks 财产. 允许指定在导出期间是否应保留分页符 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/
---
## TxtSaveOptionsBase.ForcePageBreaks property

允许指定在导出期间是否应保留分页符。

默认值为**错误的**.

```csharp
public bool ForcePageBreaks { get; set; }
```

## 评论

该属性仅影响显式插入到文档中的分页符。 与MS Word在每页末尾自动插入的分页符无关。

## 例子

显示如何指定在将文档导出为纯文本时是否保留分页符。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3");

// 创建一个“TxtSaveOptions”对象，我们可以将它传递给文档的“Save”
// 修改我们如何将文档保存为纯文本的方法。
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Aspose.Words "Document" 对象有分页符，就像 Microsoft Word 文档一样。
// 诸如“.txt”之类的保存格式是没有分页符的连续正文。
// 将“ForcePageBreaks”属性设置为“true”，以保留所有“\f”字符形式的分页符。
// 将“ForcePageBreaks”属性设置为“false”以丢弃所有分页符。
saveOptions.ForcePageBreaks = forcePageBreaks;

doc.Save(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt", saveOptions);

// 如果我们加载带有分页符的纯文本文档，
// “文档”对象将使用它们将正文拆分为页面。
doc = new Document(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt");

Assert.AreEqual(forcePageBreaks ? 3 : 1, doc.PageCount);
```

### 也可以看看

* class [TxtSaveOptionsBase](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
