---
title: TxtSaveOptionsBase.ForcePageBreaks
linktitle: ForcePageBreaks
articleTitle: ForcePageBreaks
second_title: Aspose.Words for .NET
description: 使用 TxtSaveOptionsBase 的 ForcePageBreaks 属性控制分页符。确保无缝导出并轻松维护文档格式。
type: docs
weight: 30
url: /zh/net/aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/
---
## TxtSaveOptionsBase.ForcePageBreaks property

允许指定在导出期间是否保留分页符。

默认值为`错误的`。

```csharp
public bool ForcePageBreaks { get; set; }
```

## 评论

此属性仅影响明确插入文档的分页符。 它与 MS Word 自动插入每页末尾的分页符无关。

## 例子

展示如何指定将文档导出为纯文本时是否保留分页符。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3");

// 创建一个“TxtSaveOptions”对象，我们可以将其传递给文档的“保存”
// 方法来修改我们如何将文档保存为纯文本。
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Aspose.Words“Document”对象有分页符，就像 Microsoft Word 文档一样。
// 诸如“.txt”之类的保存格式是一段连续的文本，没有分页符。
// 将“ForcePageBreaks”属性设置为“true”，以保留所有以“\f”字符形式出现的分页符。
// 将“ForcePageBreaks”属性设置为“false”以丢弃所有分页符。
saveOptions.ForcePageBreaks = forcePageBreaks;

doc.Save(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt", saveOptions);

// 如果我们加载带有分页符的纯文本文档，
// “Document”对象将使用它们将正文拆分为页面。
doc = new Document(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt");

Assert.AreEqual(forcePageBreaks ? 3 : 1, doc.PageCount);
```

### 也可以看看

* class [TxtSaveOptionsBase](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
