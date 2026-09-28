---
title: DocumentBuilderOptions.context_table_formatting property
linktitle: context_table_formatting property
articleTitle: context_table_formatting property
second_title: Aspose.Words for Python
description: "DocumentBuilderOptions.context_table_formatting property. True if the formatting applied to table content does not affect the formatting of the content that follows it"
type: docs
weight: 20
url: /ar/python-net/aspose.words/documentbuilderoptions/context_table_formatting/
---

## DocumentBuilderOptions.context_table_formatting property

True if the formatting applied to table content does not affect the formatting of the content that follows it.
Default value is ``True``.



```python
@property
def context_table_formatting(self) -> bool:
    ...

@context_table_formatting.setter
def context_table_formatting(self, value: bool):
    ...

```

### Examples

Shows how to ignore table formatting for content after.

```python
doc = aw.Document()
builder_options = aw.DocumentBuilderOptions()
builder_options.context_table_formatting = True
builder = aw.DocumentBuilder(doc=doc, options=builder_options)
# يضيف محتوى قبل الجدول.
# حجم الخط الافتراضي هو 12.
builder.writeln('Font size 12 here.')
builder.start_table()
builder.insert_cell()
# يغيّر حجم الخط داخل الجدول.
builder.font.size = 5
builder.write('Font size 5 here')
builder.insert_cell()
builder.write('Font size 5 here')
builder.end_row()
builder.end_table()
# إذا كان ContextTableFormatting صحيحًا، فإن تنسيق الجدول لا يُطبق على المحتوى التالي.
# إذا كان ContextTableFormatting خاطئًا، فإن تنسيق الجدول يُطبق على المحتوى التالي.
builder.writeln('Font size 12 here.')
doc.save(file_name=ARTIFACTS_DIR + 'Table.ContextTableFormatting.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilderOptions](../)

