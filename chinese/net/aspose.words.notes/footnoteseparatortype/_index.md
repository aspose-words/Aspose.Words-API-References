---
title: FootnoteSeparatorType Enum
linktitle: FootnoteSeparatorType
articleTitle: FootnoteSeparatorType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.FootnoteSeparatorType 枚举以自定义脚注和尾注分隔符，增强文档格式和可读性。
type: docs
weight: 5010
url: /zh/net/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enumeration

指定脚注/尾注分隔符的类型。

```csharp
public enum FootnoteSeparatorType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| FootnoteSeparator | `0` | 正文和脚注文本之间的分隔符。 |
| FootnoteContinuationSeparator | `1` | 当文本必须从上一页继续时，打印在页面的脚注文本上方。 |
| FootnoteContinuationNotice | `2` | 当脚注文本必须在后续页面上继续时，打印在页面的脚注文本下方。 |
| EndnoteSeparator | `3` | 正文和尾注文本之间的分隔符。 |
| EndnoteContinuationSeparator | `4` | 当文本必须从上一页继续时，打印在页面尾注文本上方。 |
| EndnoteContinuationNotice | `5` | 当尾注文本必须在后续页面上继续时，打印在页面尾注文本下方。 |

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

* 命名空间 [Aspose.Words.Notes](../../aspose.words.notes/)
* 部件 [Aspose.Words](../../)
