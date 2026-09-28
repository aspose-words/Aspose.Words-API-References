---
title: FieldIndex.run_subentries_on_same_line property
linktitle: run_subentries_on_same_line property
articleTitle: run_subentries_on_same_line property
second_title: Aspose.Words for Python
description: "FieldIndex.run_subentries_on_same_line property. Gets or sets whether run subentries into the same line as the main entry."
type: docs
weight: 140
url: /zh/python-net/aspose.words.fields/fieldindex/run_subentries_on_same_line/
---

## FieldIndex.run_subentries_on_same_line property

Gets or sets whether run subentries into the same line as the main entry.


```python
@property
def run_subentries_on_same_line(self) -> bool:
    ...

@run_subentries_on_same_line.setter
def run_subentries_on_same_line(self, value: bool):
    ...

```

### Examples

Shows how to work with subentries in an INDEX field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 创建一个 INDEX 字段，它将为文档中找到的每个 XE 字段显示一个条目。
# 每个条目将在左侧显示 XE 字段的 Text 属性值，
# 并在右侧显示包含 XE 字段的页面编号。
# INDEX 条目将收集所有在 "Text" 属性中具有匹配值的 XE 字段
# 合并为一个条目，而不是为每个 XE 字段创建单独的条目。
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.page_number_separator = ', see page '
index.heading = 'A'
# 具有 Text 属性且其值成为 INDEX 条目标题的 XE 字段。
# 如果此值包含由冒号分隔的两个字符串段（INDEX 条目将把 :) 视为分隔符，
# 第一个段是标题，第二个段将成为副标题。
# INDEX 字段首先按字母顺序对条目进行分组，然后，如果存在多个具有相同
# 标题的 XE 字段，INDEX 字段将进一步按这些标题的值进行子分组。
# 可以有多个子分组层，取决于多少次
# XE 字段的 Text 属性被这样分段。
# 默认情况下，INDEX 字段条目组会为该组内的每个子标题创建一个新行。
# 我们可以将 RunSubentriesOnSameLine 标志设为 true，以保持标题，
# 以及该组的所有子标题都在同一行上，这将使 INDEX 字段更紧凑。
index.run_subentries_on_same_line = run_subentries_on_the_same_line
if run_subentries_on_the_same_line:
    self.assertEqual(' INDEX  \\e ", see page " \\h A \\r', index.get_field_code())
else:
    self.assertEqual(' INDEX  \\e ", see page " \\h A', index.get_field_code())
# 插入两个 XE 字段，每个在新页面上，并使用相同的标题 "Heading 1"，
# INDEX 字段将使用该标题对它们进行分组。
# 如果 RunSubentriesOnSameLine 为 false，则 INDEX 表将创建三行：
# 一行用于分组标题 "Heading 1"，每个子标题再各占一行。
# 如果 RunSubentriesOnSameLine 为 true，则 INDEX 表将创建单行
# 条目，包含标题和所有子标题。
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Heading 1:Subheading 1'
self.assertEqual(' XE  "Heading 1:Subheading 1"', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Heading 1:Subheading 2'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + f'Field.INDEX.XE.Subheading.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

