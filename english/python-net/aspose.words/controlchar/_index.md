---
title: ControlChar class
linktitle: ControlChar class
articleTitle: ControlChar class
second_title: Aspose.Words for Python
description: "aspose.words.ControlChar class. Control characters often encountered in documents"
type: docs
weight: 260
url: /python-net/aspose.words/controlchar/
---

## ControlChar class

Control characters often encountered in documents.
To learn more, visit the [Working With Control Characters](https://docs.aspose.com/words/python-net/working-with-control-characters/) documentation article.




Provides both char and string versions of the same constants. For example:
string [ControlChar.LINE_BREAK](./LINE_BREAK/) and char [ControlChar.LINE_BREAK_CHAR](./LINE_BREAK_CHAR/) have the same value.



### Properties

| Name | Description |
| --- | --- |
| [CELL](./CELL/) | End of a table cell or end of a table row character: "\\x0007" or "\\a". |
| [CELL_CHAR](./CELL_CHAR/) | End of a table cell or end of a table row character: (char)7 or "\\a". |
| [COLUMN_BREAK](./COLUMN_BREAK/) | End of column character: "\\x000e". |
| [COLUMN_BREAK_CHAR](./COLUMN_BREAK_CHAR/) | End of column character: (char)14. |
| [CR](./CR/) | Carriage return character: "\\x000d" or "\\r". Same as [ControlChar.PARAGRAPH_BREAK](./PARAGRAPH_BREAK/). |
| [CR_LF](./CR_LF/) | Carriage return followed by line feed character: "\\x000d\\x000a" or "\\r\\n". Not used as such in Microsoft Word documents, but commonly used in text files for paragraph breaks. |
| [DEFAULT_TEXT_INPUT_CHAR](./DEFAULT_TEXT_INPUT_CHAR/) | This is the "o" character used as a default value in text input form fields. |
| [FIELD_END_CHAR](./FIELD_END_CHAR/) | End of MS Word field character: (char)21. |
| [FIELD_SEPARATOR_CHAR](./FIELD_SEPARATOR_CHAR/) | Field separator character separates field code from field value. Optional in some fields. Value: (char)20. |
| [FIELD_START_CHAR](./FIELD_START_CHAR/) | Start of MS Word field character: (char)19. |
| [LF](./LF/) | Line feed character: "\\x000a" or "\\n". Same as [ControlChar.LINE_FEED](./LINE_FEED/). |
| [LINE_BREAK](./LINE_BREAK/) | Line break character: "\\x000b" or "\\v". |
| [LINE_BREAK_CHAR](./LINE_BREAK_CHAR/) | Line break character: (char)11 or "\\v". |
| [LINE_FEED](./LINE_FEED/) | Line feed character: "\\x000a" or "\\n". Same as [ControlChar.LF](./LF/). |
| [LINE_FEED_CHAR](./LINE_FEED_CHAR/) | Line feed character: (char)10 or "\\n". |
| [NON_BREAKING_HYPHEN_CHAR](./NON_BREAKING_HYPHEN_CHAR/) | Nonbreaking Hyphen in Microsoft Word is (char)30. |
| [NON_BREAKING_SPACE](./NON_BREAKING_SPACE/) | Non-breaking space character: "\\x00a0". |
| [NON_BREAKING_SPACE_CHAR](./NON_BREAKING_SPACE_CHAR/) | Non-breaking space character: (char)160. |
| [OPTIONAL_HYPHEN_CHAR](./OPTIONAL_HYPHEN_CHAR/) | Optional Hyphen in Microsoft Word is (char)31. |
| [PAGE_BREAK](./PAGE_BREAK/) | Page break character: "\\x000c" or "\\f". Note it has the same value as [ControlChar.SECTION_BREAK](./SECTION_BREAK/). |
| [PAGE_BREAK_CHAR](./PAGE_BREAK_CHAR/) | Page break character: (char)12 or "\\f". |
| [PARAGRAPH_BREAK](./PARAGRAPH_BREAK/) | End of paragraph character: "\\x000d" or "\\r". Same as [ControlChar.CR](./CR/) |
| [PARAGRAPH_BREAK_CHAR](./PARAGRAPH_BREAK_CHAR/) | End of paragraph character: (char)13 or "\\r". |
| [SECTION_BREAK](./SECTION_BREAK/) | End of section character: "\\x000c" or "\\f". Note it has the same value as [ControlChar.PAGE_BREAK](./PAGE_BREAK/). |
| [SECTION_BREAK_CHAR](./SECTION_BREAK_CHAR/) | End of section character: (char)12 or "\\f". |
| [SPACE_CHAR](./SPACE_CHAR/) | Space character: (char)32. |
| [TAB](./TAB/) | Tab character: "\\x0009" or "\\t". |
| [TAB_CHAR](./TAB_CHAR/) | Tab character: (char)9 or "\\t". |

### Examples

Shows how to use control characters.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert paragraphs with text with DocumentBuilder.
builder.writeln("Hello world!")
builder.writeln("Hello again!")

# Converting the document to text form reveals that control characters
# represent some of the document's structural elements, such as page breaks.
self.assertEqual("Hello world!" + aw.ControlChar.CR +
                 "Hello again!" + aw.ControlChar.CR +
                 aw.ControlChar.PAGE_BREAK, doc.get_text())

# When converting a document to string form,
# we can omit some of the control characters with the "strip" method.
self.assertEqual("Hello world!" + aw.ControlChar.CR +
                 "Hello again!", doc.get_text().strip())
```

### See Also

* module [aspose.words](../)

