---
title: TextWrapping enumeration
linktitle: TextWrapping enumeration
articleTitle: TextWrapping enumeration
second_title: Aspose.Words for Python
description: "aspose.words.tables.TextWrapping enumeration. Specifies how text is wrapped around the table."
type: docs
weight: 160
url: /ru/python-net/aspose.words.tables/textwrapping/
---

## TextWrapping enumeration

Specifies how text is wrapped around the table.


### Members

| Name | Description |
| --- | --- |
| NONE | Text and table is displayed in the order of their appearance in the document. |
| AROUND | Text is wrapped around the table occupying available side space. |
| DEFAULT | Default value. |

### Examples

Shows how to work with table text wrapping.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
table = builder.start_table()
builder.insert_cell()
builder.write('Cell 1')
builder.insert_cell()
builder.write('Cell 2')
builder.end_table()
table.preferred_width = aw.tables.PreferredWidth.from_points(300)
builder.font.size = 16
builder.writeln('Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
# Установите свойство "TextWrapping" в значение "TextWrapping.Around", чтобы таблица обтекала текст вокруг неё,
# и опустите её в следующий абзац, задав позицию.
table.text_wrapping = aw.tables.TextWrapping.AROUND
table.absolute_horizontal_distance = 100
table.absolute_vertical_distance = 20
doc.save(file_name=ARTIFACTS_DIR + 'Table.WrapText.docx')
```

### See Also

* module [aspose.words.tables](../)

