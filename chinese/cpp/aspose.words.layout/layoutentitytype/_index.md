---
title: "Aspose::Words::Layout::LayoutEntityType 枚举"
linktitle: "LayoutEntityType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::LayoutEntityType 枚举。C++ 中布局实体的类型。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.layout/layoutentitytype/
---
## LayoutEntityType enum


布局实体的类型。

```cpp
enum class LayoutEntityType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | n/a | 默认值。 |
| Page | n/a | 表示文档的页面。页面可能包含 [Column](./)、[HeaderFooter](./) 和 [Comment](./) 子实体。 |
| Column | n/a | 表示页面上的文本列。列可能拥有与 [Cell](./) 相同的子实体，以及 [Footnote](./)、[Endnote](./) 和 [NoteSeparator](./) 实体。 |
| Row | n/a | 表示表格行。行可能以 [Cell](./) 作为子实体。 |
| Cell | n/a | 表示表格单元格。单元格可能包含 [Line](./) 和 [Row](./) 子实体。 |
| Line | n/a | 表示文本字符行和内联对象。行可能包含 [Span](./) 子实体。 |
| Span | n/a | 表示行中的一个或多个字符。包括字段开始/结束标记、书签和注释等特殊字符。Span 不能拥有子实体。 |
| Footnote | n/a | 表示脚注内容的占位符。脚注可能包含 [Note](./) 子实体。 |
| Endnote | n/a | 表示尾注内容的占位符。尾注可能包含 [Note](./) 子实体。 |
| Note | n/a | 表示注释内容的占位符。Note 可能拥有 [Line](./) 和 [Row](./) 子实体。 |
| HeaderFooter | n/a | 表示页面上页眉/页脚内容的占位符。[HeaderFooter](../../aspose.words/headerfooter/) 可能包含 [Line](./) 和 [Row](./) 子实体。 |
| TextBox | n/a | 表示形状内部的文本区域。Textbox 可能包含 [Line](./) 和 [Row](./) 子实体。 |
| Comment | n/a | 表示注释内容的占位符。[Comment](../../aspose.words/comment/) 可能拥有 [Line](./) 和 [Row](./) 子实体。 |
| NoteSeparator | n/a | 表示脚注/尾注分隔符。NoteSeparator 可能包含 [Line](./) 和 [Row](./) 子实体。 |

## 另见

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
