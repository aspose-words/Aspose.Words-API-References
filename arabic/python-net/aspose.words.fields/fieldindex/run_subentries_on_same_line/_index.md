---
title: FieldIndex.run_subentries_on_same_line property
linktitle: run_subentries_on_same_line property
articleTitle: run_subentries_on_same_line property
second_title: Aspose.Words for Python
description: "FieldIndex.run_subentries_on_same_line property. Gets or sets whether run subentries into the same line as the main entry."
type: docs
weight: 140
url: /ar/python-net/aspose.words.fields/fieldindex/run_subentries_on_same_line/
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
# أنشئ حقل INDEX سيعرض إدخالًا لكل حقل XE موجود في المستند.
# سيعرض كل إدخال قيمة خاصية Text لحقل XE على الجانب الأيسر،
# ورقم الصفحة التي تحتوي على حقل XE على الجانب الأيمن.
# سيتجمع إدخال INDEX جميع حقول XE ذات القيم المطابقة في خاصية "Text"
# في إدخال واحد بدلاً من إنشاء إدخال لكل حقل XE.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.page_number_separator = ', see page '
index.heading = 'A'
# حقول XE التي لديها خاصية Text التي تصبح قيمتها عنوان إدخال INDEX.
# إذا كانت هذه القيمة تحتوي على جزأين نصيين مقسومين بنقطتين (:)، سيتعامل إدخال INDEX مع الفاصل :) ،
# الجزء الأول هو العنوان، والجزء الثاني سيصبح العنوان الفرعي.
# يقوم حقل INDEX أولاً بتجميع الإدخالات أبجديًا، ثم إذا كان هناك عدة حقول XE بنفس
# العناوين، سيقوم حقل INDEX بتقسيمها فرعيًا بناءً على قيم هذه العناوين.
# يمكن أن تكون هناك طبقات فرعية متعددة، اعتمادًا على عدد المرات
# التي يتم فيها تقسيم خصائص Text لحقول XE بهذه الطريقة.
# بشكل افتراضي، سيُنشئ مجموعة إدخالات حقل INDEX سطرًا جديدًا لكل عنوان فرعي داخل هذه المجموعة.
# يمكننا تعيين علامة RunSubentriesOnSameLine إلى true للحفاظ على العنوان،
# وكل عنوان فرعي للمجموعة في سطر واحد بدلاً من ذلك، مما سيجعل حقل INDEX أكثر تكثيفًا.
index.run_subentries_on_same_line = run_subentries_on_the_same_line
if run_subentries_on_the_same_line:
    self.assertEqual(' INDEX  \\e ", see page " \\h A \\r', index.get_field_code())
else:
    self.assertEqual(' INDEX  \\e ", see page " \\h A', index.get_field_code())
# أدخل حقلين XE، كلٌ على صفحة جديدة، وبنفس العنوان المسمى "Heading 1",
# الذي سيستخدمه حقل INDEX لتجميعهما.
# إذا كان RunSubentriesOnSameLine false، فستُنشئ جدول INDEX ثلاثة أسطر:
# سطر واحد لعنوان التجميع "Heading 1"، وسطر إضافي لكل عنوان فرعي.
# إذا كان RunSubentriesOnSameLine true، فستُنشئ جدول INDEX سطرًا واحدًا
# يحتوي على العنوان وكل عنوان فرعي.
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

