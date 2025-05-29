---
title: DocumentBase.FootnoteSeparators
linktitle: FootnoteSeparators
articleTitle: FootnoteSeparators
second_title: Aspose.Words for .NET
description: 使用 DocumentBase 的 FootnoteSeparators 属性访问和自定义文档中的脚注和尾注分隔符，以增强格式控制。
type: docs
weight: 40
url: /zh/net/aspose.words/documentbase/footnoteseparators/
---
## DocumentBase.FootnoteSeparators property

提供对文档中定义的脚注/尾注分隔符的访问。

```csharp
public FootnoteSeparatorCollection FootnoteSeparators { get; }
```

## 例子

显示如何删除尾注分隔符。

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator endnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.EndnoteSeparator];
// 删除尾注分隔符。
endnoteSeparator.FirstParagraph.FirstChild.Remove();
```

显示如何管理脚注分隔符格式。

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// 对齐脚注分隔符。
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### 也可以看看

* class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* class [DocumentBase](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
