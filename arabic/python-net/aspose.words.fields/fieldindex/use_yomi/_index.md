---
title: FieldIndex.use_yomi property
linktitle: use_yomi property
articleTitle: use_yomi property
second_title: Aspose.Words for Python
description: "FieldIndex.use_yomi property. Gets or sets whether to enable the use of yomi text for index entries."
type: docs
weight: 170
url: /ar/python-net/aspose.words.fields/fieldindex/use_yomi/
---

## FieldIndex.use_yomi property

Gets or sets whether to enable the use of yomi text for index entries.


```python
@property
def use_yomi(self) -> bool:
    ...

@use_yomi.setter
def use_yomi(self, value: bool):
    ...

```

### Examples

Shows how to sort INDEX field entries phonetically.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أنشئ حقل INDEX سيعرض إدخالًا لكل حقل XE موجود في المستند.
# سيعرض كل إدخال قيمة خاصية Text لحقل XE على الجانب الأيسر،
# ورقم الصفحة التي تحتوي على حقل XE على الجانب الأيمن.
# سيتجمع إدخال INDEX جميع حقول XE ذات القيم المطابقة في خاصية "Text"
# في إدخال واحد بدلاً من إنشاء إدخال لكل حقل XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# يقوم جدول INDEX بترتيب إدخالاته تلقائيًا حسب قيم خصائص Text الخاصة بها بترتيب أبجدي.
# اضبط جدول INDEX لترتيب الإدخالات صوتيًا باستخدام الهيراغانا بدلاً من ذلك.
index.use_yomi = sort_entries_using_yomi
if sort_entries_using_yomi:
    self.assertEqual(' INDEX  \\y', index.get_field_code())
else:
    self.assertEqual(' INDEX ', index.get_field_code())
# أدرج 4 حقول XE، والتي ستظهر كإدخالات في جدول محتويات حقل INDEX.
# قد يحتوي خاصية "Text" على تهجئة كلمة بالكانجي، والتي قد يكون نطقها غامضًا،
# في حين أن نسخة "Yomi" من الكلمة ستهجئ بالضبط كما تُنطق باستخدام الهيراغانا.
# إذا قمنا بتعيين حقل INDEX لاستخدام Yomi، فسيتم فرز هذه الإدخالات
# حسب قيمة خصائص Yomi الخاصة بها، بدلاً من قيم Text.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '愛子'
index_entry.yomi = 'あ'
self.assertEqual(' XE  愛子 \\y あ', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '明美'
index_entry.yomi = 'あ'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '恵美'
index_entry.yomi = 'え'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = '愛美'
index_entry.yomi = 'え'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Yomi.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

