---
title: Document.IncludeTextboxesFootnotesEndnotesInStat
linktitle: IncludeTextboxesFootnotesEndnotesInStat
articleTitle: IncludeTextboxesFootnotesEndnotesInStat
second_title: Aspose.Words for .NET
description: 使用 IncludeTextboxesFootnotesEndnotesInStat 属性优化文档的字数统计。轻松控制文本框、脚注和尾注！
type: docs
weight: 230
url: /zh/net/aspose.words/document/includetextboxesfootnotesendnotesinstat/
---
## Document.IncludeTextboxesFootnotesEndnotesInStat property

指定是否在字数统计中包含文本框、脚注和尾注。

```csharp
public bool IncludeTextboxesFootnotesEndnotesInStat { get; set; }
```

## 例子

展示如何在字数统计中包含或排除文本框、脚注和尾注。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Lorem ipsum");
builder.InsertFootnote(FootnoteType.Footnote, "sit amet");

// 默认选项设置为“false”。
doc.UpdateWordCount();
// 字数计算不包括文本框、脚注和尾注。
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Words);

doc.IncludeTextboxesFootnotesEndnotesInStat = true;
doc.UpdateWordCount();
// 使用文本框、脚注和尾注来计算字数。
Assert.AreEqual(4, doc.BuiltInDocumentProperties.Words);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
