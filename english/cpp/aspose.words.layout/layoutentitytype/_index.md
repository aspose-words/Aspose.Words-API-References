---
title: Aspose::Words::Layout::LayoutEntityType enum
linktitle: LayoutEntityType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::LayoutEntityType enum. Types of the layout entities in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.layout/layoutentitytype/
---
## LayoutEntityType enum


Types of the layout entities.

```cpp
enum class LayoutEntityType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | n/a | Default value. |
| Page | n/a | Represents page of a document. Page may have [Column](./), [HeaderFooter](./) and [Comment](./) child entities. |
| Column | n/a | Represents a column of text on a page. Column may have the same child entities as [Cell](./), plus [Footnote](./), [Endnote](./) and [NoteSeparator](./) entities. |
| Row | n/a | Represents a table row. Row may have [Cell](./) as child entities. |
| Cell | n/a | Represents a table cell. Cell may have [Line](./) and [Row](./) child entities. |
| Line | n/a | Represents line of characters of text and inline objects. Line may have [Span](./) child entities. |
| Span | n/a | Represents one or more characters in a line. This include special characters like field start/end markers, bookmarks and comments. Span may not have child entities. |
| Footnote | n/a | Represents placeholder for footnote content. Footnote may have [Note](./) child entities. |
| Endnote | n/a | Represents placeholder for endnote content. Endnote may have [Note](./) child entities. |
| Note | n/a | Represents placeholder for note content. Note may have [Line](./) and [Row](./) child entities. |
| HeaderFooter | n/a | Represents placeholder for header/footer content on a page. [HeaderFooter](../../aspose.words/headerfooter/) may have [Line](./) and [Row](./) child entities. |
| TextBox | n/a | Represents text area inside of a shape. Textbox may have [Line](./) and [Row](./) child entities. |
| Comment | n/a | Represents placeholder for comment content. [Comment](../../aspose.words/comment/) may have [Line](./) and [Row](./) child entities. |
| NoteSeparator | n/a | Represents footnote/endnote separator. NoteSeparator may have [Line](./) and [Row](./) child entities. |

## See Also

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
