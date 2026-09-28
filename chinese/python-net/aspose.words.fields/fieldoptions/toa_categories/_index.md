---
title: FieldOptions.toa_categories property
linktitle: toa_categories property
articleTitle: toa_categories property
second_title: Aspose.Words for Python
description: "FieldOptions.toa_categories property. Gets or sets the table of authorities categories."
type: docs
weight: 190
url: /zh/python-net/aspose.words.fields/fieldoptions/toa_categories/
---

## FieldOptions.toa_categories property

Gets or sets the table of authorities categories.


```python
@property
def toa_categories(self) -> aspose.words.fields.ToaCategories:
    ...

@toa_categories.setter
def toa_categories(self, value: aspose.words.fields.ToaCategories):
    ...

```

### Examples

Shows how to specify a set of categories for TOA fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# TOA 字段可以通过此集合中定义的类别过滤其条目。
toa_categories = aw.fields.ToaCategories()
doc.field_options.toa_categories = toa_categories
# 此类别集合带有默认值，我们可以用自定义值覆盖它们。
self.assertEqual('Cases', toa_categories[1])
self.assertEqual('Statutes', toa_categories[2])
toa_categories[1] = 'My Category 1'
toa_categories[2] = 'My Category 2'
# 我们始终可以通过此集合访问默认值。
self.assertEqual('Cases', aw.fields.ToaCategories.default_categories[1])
self.assertEqual('Statutes', aw.fields.ToaCategories.default_categories[2])
# 插入 2 个 TOA 字段。TOA 字段为文档中的每个 TA 字段创建一个条目。
# 使用 "\c" 开关从我们的集合中选择类别的索引。
#  使用此开关，TOA 字段只会获取来自 TA 字段的条目，这些字段
# 也具有匹配类别索引的 "\c" 开关。每个 TOA 字段还将显示
# 其 "\c" 开关指向的类别名称。
builder.insert_field(field_code='TOA \\c 1 \\h', field_value=None)
builder.insert_field(field_code='TOA \\c 2 \\h', field_value=None)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# 在 2 个类别中插入 TOA 条目。我们的第一个 TOA 字段将接收一个条目，
# 来自第二个 TA 字段，该字段的 "\c" 开关也指向第一个类别。
# 第二个 TOA 字段将拥有来自另外两个 TA 字段的两个条目。
builder.insert_field(field_code='TA \\c 2 \\l "entry 1"')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_field(field_code='TA \\c 1 \\l "entry 2"')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_field(field_code='TA \\c 2 \\l "entry 3"')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'FieldOptions.TOA.Categories.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

