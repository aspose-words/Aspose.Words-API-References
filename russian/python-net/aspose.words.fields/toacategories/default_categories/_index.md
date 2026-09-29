---
title: ToaCategories.default_categories property
linktitle: default_categories property
articleTitle: default_categories property
second_title: Aspose.Words for Python
description: "ToaCategories.default_categories property. Gets the default table of authorities categories."
type: docs
weight: 30
url: /ru/python-net/aspose.words.fields/toacategories/default_categories/
---

## ToaCategories.default_categories property

Gets the default table of authorities categories.


```python
@property
def default_categories(self) -> aspose.words.fields.ToaCategories:
    ...

```

### Remarks

Use the [FieldOptions.toa_categories](../../fieldoptions/toa_categories/) property to specify table of authorities categories for a single document.



### Examples

Shows how to specify a set of categories for TOA fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Поля TOA могут фильтровать свои записи по категориям, определённым в этой коллекции.
toa_categories = aw.fields.ToaCategories()
doc.field_options.toa_categories = toa_categories
# Эта коллекция категорий поставляется со значениями по умолчанию, которые мы можем перезаписать пользовательскими значениями.
self.assertEqual('Cases', toa_categories[1])
self.assertEqual('Statutes', toa_categories[2])
toa_categories[1] = 'My Category 1'
toa_categories[2] = 'My Category 2'
# Мы всегда можем получить доступ к значениям по умолчанию через эту коллекцию.
self.assertEqual('Cases', aw.fields.ToaCategories.default_categories[1])
self.assertEqual('Statutes', aw.fields.ToaCategories.default_categories[2])
# Вставьте 2 поля TOA. Поля TOA создают запись для каждого поля TA в документе.
# Используйте переключатель "\c", чтобы выбрать индекс категории из нашей коллекции.
#  С помощью этого переключателя поле TOA будет получать записи только из полей TA, которые
# также имеют переключатель "\c" с соответствующим индексом категории. Каждое поле TOA также будет отображать
# название категории, на которую указывает его переключатель "\c".
builder.insert_field(field_code='TOA \\c 1 \\h', field_value=None)
builder.insert_field(field_code='TOA \\c 2 \\h', field_value=None)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Вставьте записи TOA в 2 категории. Наше первое поле TOA получит одну запись,
# из второго поля TA, чей переключатель "\c" также указывает на первую категорию.
# Второе поле TOA будет иметь две записи из остальных двух полей TA.
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
* class [ToaCategories](../)

