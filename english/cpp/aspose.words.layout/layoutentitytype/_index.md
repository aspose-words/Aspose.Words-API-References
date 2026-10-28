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
enum class LayoutEntityType : int
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Cell | 16 | Represents a table cell. Cell may have [Line](./) and [Row](./) child entities. |
| Column | 2 | Represents a column of text on a page. Column may have the same child entities as [Cell](./), plus [Footnote](./), [Endnote](./) and [NoteSeparator](./) entities. |
| Comment | 4096 | Represents placeholder for comment content. Comment may have [Line](./) and [Row](./) child entities. |
| Endnote | 512 | Represents placeholder for endnote content. Endnote may have [Note](./) child entities. |
| Footnote | 256 | Represents placeholder for footnote content. Footnote may have [Note](./) child entities. |
| HeaderFooter | 1024 | Represents placeholder for header/footer content on a page. HeaderFooter may have [Line](./) and [Row](./) child entities. |
| Line | 32 | Represents line of characters of text and inline objects. Line may have [Span](./) child entities. |
| None | 0 | Default value. |
| Note | 16384 | Represents placeholder for note content. Note may have [Line](./) and [Row](./) child entities. |
| NoteSeparator | 8192 | Represents footnote/endnote separator. NoteSeparator may have [Line](./) and [Row](./) child entities. |
| Page | 1 | Represents page of a document. Page may have [Column](./), [HeaderFooter](./) and [Comment](./) child entities. |
| Row | 8 | Represents a table row. Row may have [Cell](./) as child entities. |
| Span | 64 | Represents one or more characters in a line. This include special characters like field start/end markers, bookmarks and comments. Span may not have child entities. |
| TextBox | 2048 | Represents text area inside of a shape. Textbox may have [Line](./) and [Row](./) child entities. |

## See Also

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
