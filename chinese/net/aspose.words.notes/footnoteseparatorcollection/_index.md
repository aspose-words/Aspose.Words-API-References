---
title: FootnoteSeparatorCollection Class
linktitle: FootnoteSeparatorCollection
articleTitle: FootnoteSeparatorCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Notes.FootnoteSeparatorCollection，轻松访问文档中的脚注分隔符。立即增强您的文档格式！
type: docs
weight: 5000
url: /zh/net/aspose.words.notes/footnoteseparatorcollection/
---
## FootnoteSeparatorCollection class

提供对[`FootnoteSeparator`](../footnoteseparator/)文档的节点。

```csharp
public class FootnoteSeparatorCollection : IEnumerable<FootnoteSeparator>
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FootnoteSeparatorCollection](footnoteseparatorcollection/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Item](../../aspose.words.notes/footnoteseparatorcollection/item/) { get; } | 检索[`FootnoteSeparator`](../footnoteseparator/)指定类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetEnumerator](../../aspose.words.notes/footnoteseparatorcollection/getenumerator/)() |  |

## 例子

显示如何管理脚注分隔符格式。

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// 对齐脚注分隔符。
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### 也可以看看

* class [FootnoteSeparator](../footnoteseparator/)
* 命名空间 [Aspose.Words.Notes](../../aspose.words.notes/)
* 部件 [Aspose.Words](../../)
