---
title: FieldIndex.sequence_separator property
linktitle: sequence_separator property
articleTitle: sequence_separator property
second_title: Aspose.Words for Python
description: "FieldIndex.sequence_separator property. Gets or sets the character sequence that is used to separate sequence numbers and page numbers."
type: docs
weight: 160
url: /ar/python-net/aspose.words.fields/fieldindex/sequence_separator/
---

## FieldIndex.sequence_separator property

Gets or sets the character sequence that is used to separate sequence numbers and page numbers.


```python
@property
def sequence_separator(self) -> str:
    ...

@sequence_separator.setter
def sequence_separator(self, value: str):
    ...

```

### Examples

Shows how to split a document into portions by combining INDEX and SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أنشئ حقل INDEX سيعرض إدخالًا لكل حقل XE موجود في المستند.
# سيعرض كل إدخال قيمة خاصية Text لحقل XE على الجانب الأيسر،
# ورقم الصفحة التي تحتوي على حقل XE على الجانب الأيمن.
# إذا كانت حقول XE لها نفس القيمة في خاصية "Text" الخاصة بها،
# سيقوم حقل INDEX بتجميعها في إدخال واحد.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# في خاصية SequenceName، قم بتسمية تسلسل حقل SEQ. كل إدخال في حقل INDEX سيعرض الآن أيضًا
# الرقم الذي يكون عليه عدّ التسلسل في موقع حقل XE الذي أنشأ هذا الإدخال.
index.sequence_name = 'MySequence'
# حدد نصًا سيحيط بالتسلسل وأرقام الصفحات لشرح معناها للمستخدم.
# سيعرض إدخال تم إنشاؤه بهذه التكوين شيئًا مثل "MySequence at 1 on page 1" عند رقم صفحته.
# لا يمكن أن يكون PageNumberSeparator و SequenceSeparator أطول من 15 حرفًا.
index.page_number_separator = '\tMySequence at '
index.sequence_separator = ' on page '
self.assertTrue(index.has_sequence_name)
self.assertEqual(' INDEX  \\s MySequence \\e "\tMySequence at " \\d " on page "', index.get_field_code())
# حقول SEQ تعرض عدًّا يزداد عند كل حقل SEQ.
# هذه الحقول تحافظ أيضًا على عدادات منفصلة لكل تسلسل مسمى فريد
# محددة بواسطة خاصية "SequenceIdentifier" لحقل SEQ.
# أدرج حقل SEQ الذي ينقل تسلسل "MySequence" إلى 1.
# هذا الحقل لا يختلف عن نص المستند العادي. لن يظهر في جدول محتويات حقل INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', sequence_field.get_field_code())
# أدرج حقل XE الذي سيُنشئ إدخالًا في حقل INDEX.
# نظرًا لأن "MySequence" هو عند 1 وهذا الحقل XE على الصفحة 2، إلى جانب الفواصل المخصصة التي عرّفناها أعلاه،
# سيعرض إدخال INDEX لهذا الحقل "Cat" على الجانب الأيسر، و"MySequence at 1 on page 2" على الجانب الأيمن.
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cat'
self.assertEqual(' XE  Cat', index_entry.get_field_code())
# أدرج فاصل صفحة واستخدم حقول SEQ لتقدم "MySequence" إلى 3.
builder.insert_break(aw.BreakType.PAGE_BREAK)
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
sequence_field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
sequence_field.sequence_identifier = 'MySequence'
# أدرج حقل XE بنفس خاصية Text كما في السابق.
# سوف يجمع إدخال INDEX حقول XE ذات القيم المتطابقة في خاصية "Text"
# في إدخال واحد بدلاً من إنشاء إدخال لكل حقل XE.
# نظرًا لأننا على الصفحة 2 مع "MySequence" عند 3، سيتم إلحاق ", 3 on page 3" إلى نفس إدخال INDEX كما في الأعلى.
# ستعرض الآن جزء رقم الصفحة من ذلك الإدخال INDEX "MySequence at 1 on page 2, 3 on page 3".
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cat'
# أدرج حقل XE بقيمة خاصية Text جديدة وفريدة.
# سيضيف هذا إدخالًا جديدًا، مع MySequence عند 3 على الصفحة 4.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Dog'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Sequence.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldIndex](../)

