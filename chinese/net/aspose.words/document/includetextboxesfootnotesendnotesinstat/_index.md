---
title: Document.IncludeTextboxesFootnotesEndnotesInStat
linktitle: IncludeTextboxesFootnotesEndnotesInStat
articleTitle: IncludeTextboxesFootnotesEndnotesInStat
second_title: 用于 .NET 的 Aspose.Words
description: Document IncludeTextboxesFootnotesEndnotesInStat 财产. 指定字数统计中是否包括文本框脚注和尾注 在 C#.
type: docs
weight: 220
url: /zh/net/aspose.words/document/includetextboxesfootnotesendnotesinstat/
---
## Document.IncludeTextboxesFootnotesEndnotesInStat property

指定字数统计中是否包括文本框、脚注和尾注。

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

// 默认情况下选项设置为“false”。
doc.UpdateWordCount();
// 不计文本框、脚注和尾注的字数。
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Words);            

doc.IncludeTextboxesFootnotesEndnotesInStat = true;
doc.UpdateWordCount();
// 文本框、脚注和尾注的字数统计。
Assert.AreEqual(4, doc.BuiltInDocumentProperties.Words);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
