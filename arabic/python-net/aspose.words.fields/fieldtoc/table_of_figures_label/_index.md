---
title: FieldToc.table_of_figures_label property
linktitle: table_of_figures_label property
articleTitle: table_of_figures_label property
second_title: Aspose.Words for Python
description: "FieldToc.table_of_figures_label property. Gets or sets the name of the sequence identifier used when building a table of figures."
type: docs
weight: 160
url: /ar/python-net/aspose.words.fields/fieldtoc/table_of_figures_label/
---

## FieldToc.table_of_figures_label property

Gets or sets the name of the sequence identifier used when building a table of figures.


```python
@property
def table_of_figures_label(self) -> str:
    ...

@table_of_figures_label.setter
def table_of_figures_label(self, value: str):
    ...

```

### Examples

Shows how to populate a TOC field with entries using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# يمكن لحقل TOC إنشاء إدخال في جدول المحتويات لكل حقل SEQ موجود في المستند.
# كل إدخال يحتوي على الفقرة التي تشمل حقل SEQ ورقم الصفحة التي يظهر فيها الحقل.
field_toc = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOC, update_field=True).as_field_toc()
# حقول SEQ تعرض عدًّا يزداد عند كل حقل SEQ.
# هذه الحقول تحافظ أيضًا على عدادات منفصلة لكل تسلسل مسمى فريد
# محددة بواسطة خاصية "SequenceIdentifier" لحقل SEQ.
# استخدم خاصية "TableOfFiguresLabel" لتسمية تسلسل رئيسي للـ TOC.
# الآن، سيقوم هذا الـ TOC بإنشاء إدخالات فقط من حقول SEQ التي تم تعيين "SequenceIdentifier" لها إلى "MySequence".
field_toc.table_of_figures_label = 'MySequence'
# يمكننا تسمية تسلسل حقل SEQ آخر في خاصية "PrefixedSequenceIdentifier".
# حقول SEQ من هذا التسلسل المسبق لن تنشئ إدخالات TOC.
# كل إدخال TOC تم إنشاؤه من حقل SEQ لتسلسل رئيسي سيعرض الآن أيضًا العد الذي
# التسلسل السابق حاليًا في حقل SEQ التسلسل الأساسي الذي أنشأ الإدخال.
field_toc.prefixed_sequence_identifier = 'PrefixSequence'
# سيعرض كل إدخال TOC عدد التسلسل السابق مباشرةً إلى اليسار
# من رقم الصفحة التي يظهر فيها حقل SEQ التسلسل الرئيسي.
# يمكننا تحديد فاصل مخصص سيظهر بين هذين الرقمين.
field_toc.sequence_separator = '>'
self.assertEqual(' TOC  \\c MySequence \\s PrefixSequence \\d >', field_toc.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# هناك طريقتان لاستخدام حقول SEQ لملء هذا TOC.
# 1 - إدراج حقل SEQ ينتمي إلى تسلسل البادئة في TOC:
# سيزيد هذا الحقل عدد تسلسل SEQ لـ "PrefixSequence" بمقدار 1.
# نظرًا لأن هذا الحقل لا ينتمي إلى التسلسل الرئيسي المحدد
# بواسطة خاصية "TableOfFiguresLabel" في TOC، لن يظهر كإدخال.
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
self.assertEqual(' SEQ  PrefixSequence', field_seq.get_field_code())
# 2 - إدراج حقل SEQ ينتمي إلى التسلسل الرئيسي في TOC:
# سيُنشئ حقل SEQ هذا إدخالًا في TOC.
# سيتضمن إدخال TOC الفقرة التي يوجد فيها حقل SEQ ورقم الصفحة التي يظهر فيها.
# سيعرض هذا الإدخال أيضًا العدد الذي وصل إليه التسلسل السابق حاليًا،
# مفصولًا عن رقم الصفحة بالقيمة الموجودة في خاصية SeqenceSeparator في TOC.
# العدد "PrefixSequence" هو 1، وحقل SEQ التسلسل الرئيسي على الصفحة 2،
# والفاصل هو ">"، لذا سيعرض الإدخال "1>2".
builder.write('First TOC entry, MySequence #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
self.assertEqual(' SEQ  MySequence', field_seq.get_field_code())
# أدرج صفحة، وقدم التسلسل السابق بمقدار 2، ثم أدرج حقل SEQ لإنشاء إدخال TOC لاحقًا.
# التسلسل السابق الآن هو 2، وحقل SEQ التسلسل الرئيسي على الصفحة 3،
# لذا سيعرض إدخال TOC "2>3" في عدد صفحته.
builder.insert_break(aw.BreakType.PAGE_BREAK)
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'PrefixSequence'
builder.insert_paragraph()
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
builder.write('Second TOC entry, MySequence #')
field_seq.sequence_identifier = 'MySequence'
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOC.SEQ.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldToc](../)

