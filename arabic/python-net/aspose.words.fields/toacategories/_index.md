---
title: ToaCategories class
linktitle: ToaCategories class
articleTitle: ToaCategories class
second_title: Aspose.Words for Python
description: "aspose.words.fields.ToaCategories class. Represents a table of authorities categories"
type: docs
weight: 1320
url: /ar/python-net/aspose.words.fields/toacategories/
---

## ToaCategories class

Represents a table of authorities categories.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [ToaCategories()](./__init__/#default) | The default constructor. |

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets or sets the category heading by category number. |

### Properties

| Name | Description |
| --- | --- |
| [default_categories](./default_categories/) | Gets the default table of authorities categories. |

### Examples

Shows how to specify a set of categories for TOA fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# يمكن لحقول TOA تصفية مدخلاتها حسب الفئات المعرفة في هذه المجموعة.
toa_categories = aw.fields.ToaCategories()
doc.field_options.toa_categories = toa_categories
# تأتي هذه المجموعة من الفئات بقيم افتراضية، يمكننا استبدالها بقيم مخصصة.
self.assertEqual('Cases', toa_categories[1])
self.assertEqual('Statutes', toa_categories[2])
toa_categories[1] = 'My Category 1'
toa_categories[2] = 'My Category 2'
# يمكننا دائمًا الوصول إلى القيم الافتراضية عبر هذه المجموعة.
self.assertEqual('Cases', aw.fields.ToaCategories.default_categories[1])
self.assertEqual('Statutes', aw.fields.ToaCategories.default_categories[2])
# أدرج حقلين TOA. تقوم حقول TOA بإنشاء إدخال لكل حقل TA في المستند.
# استخدم المفتاح "\c" لتحديد فهرس الفئة من مجموعتنا.
#  باستخدام هذا المفتاح، سيختار حقل TOA فقط الإدخالات من حقول TA التي
# تحتوي أيضًا على مفتاح "\c" مع فهرس فئة مطابق. سيعرض كل حقل TOA أيضًا
# اسم الفئة التي يشير إليه مفتاح "\c" الخاص به.
builder.insert_field(field_code='TOA \\c 1 \\h', field_value=None)
builder.insert_field(field_code='TOA \\c 2 \\h', field_value=None)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# أدرج إدخالات TOA عبر فئتين. سيستقبل حقل TOA الأول لدينا إدخالًا واحدًا،
# من الحقل الثاني TA الذي يشير مفتاح "\c" الخاص به أيضًا إلى الفئة الأولى.
# سيحتوي حقل TOA الثاني على إدخالين من الحقلين TA الآخرين.
builder.insert_field(field_code='TA \\c 2 \\l "entry 1"')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_field(field_code='TA \\c 1 \\l "entry 2"')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_field(field_code='TA \\c 2 \\l "entry 3"')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'FieldOptions.TOA.Categories.docx')
```

### See Also

* module [aspose.words.fields](../)

