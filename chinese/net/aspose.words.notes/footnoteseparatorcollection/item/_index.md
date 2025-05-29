---
title: FootnoteSeparatorCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: 访问 FootnoteSeparatorCollection Item 属性，轻松按类型检索自定义 FootnoteSeparators，增强文档格式。
type: docs
weight: 20
url: /zh/net/aspose.words.notes/footnoteseparatorcollection/item/
---
## FootnoteSeparatorCollection indexer

检索[`FootnoteSeparator`](../../footnoteseparator/)指定类型。

```csharp
public FootnoteSeparator this[FootnoteSeparatorType separatorType] { get; }
```

## 评论

返回`无效的`如果未找到指定类型的脚注/尾注分隔符。

## 例子

显示如何管理脚注分隔符格式。

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// 对齐脚注分隔符。
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### 也可以看看

* class [FootnoteSeparator](../../footnoteseparator/)
* enum [FootnoteSeparatorType](../../footnoteseparatortype/)
* class [FootnoteSeparatorCollection](../)
* 命名空间 [Aspose.Words.Notes](../../../aspose.words.notes/)
* 部件 [Aspose.Words](../../../)
