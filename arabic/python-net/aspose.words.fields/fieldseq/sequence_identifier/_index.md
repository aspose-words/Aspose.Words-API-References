---
title: FieldSeq.sequence_identifier property
linktitle: sequence_identifier property
articleTitle: sequence_identifier property
second_title: Aspose.Words for Python
description: "FieldSeq.sequence_identifier property. Gets or sets the name assigned to the series of items that are to be numbered."
type: docs
weight: 60
url: /ar/python-net/aspose.words.fields/fieldseq/sequence_identifier/
---

## FieldSeq.sequence_identifier property

Gets or sets the name assigned to the series of items that are to be numbered.


```python
@property
def sequence_identifier(self) -> str:
    ...

@sequence_identifier.setter
def sequence_identifier(self, value: str):
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

Shows create numbering using SEQ fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# حقول SEQ تعرض عدًّا يزداد عند كل حقل SEQ.
# هذه الحقول تحافظ أيضًا على عدادات منفصلة لكل تسلسل مسمى فريد
# محددة بواسطة خاصية "SequenceIdentifier" لحقل SEQ.
# أدرج حقل SEQ سيعرض قيمة العدد الحالي لـ "MySequence",
# بعد استخدام خاصية "ResetNumber" لتعيينه إلى 100.
builder.write('#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_number = '100'
field_seq.update()
self.assertEqual(' SEQ  MySequence \\r 100', field_seq.get_field_code())
self.assertEqual('100', field_seq.result)
# اعرض الرقم التالي في هذا التسلسل باستخدام حقل SEQ آخر.
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.update()
self.assertEqual('101', field_seq.result)
# أدرج عنوان مستوى 1.
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('This level 1 heading will reset MySequence to 1')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
# أدرج حقل SEQ آخر من نفس التسلسل وقم بضبطه لإعادة تعيين العدد عند كل عنوان إلى 1.
builder.write('\n#')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.reset_heading_level = '1'
field_seq.update()
# العنوان أعلاه هو عنوان مستوى 1، لذا يتم إعادة تعيين العدد لهذا التسلسل إلى 1.
self.assertEqual(' SEQ  MySequence \\s 1', field_seq.get_field_code())
self.assertEqual('1', field_seq.result)
# انتقل إلى الرقم التالي في هذه السلسلة.
builder.write(', #')
field_seq = builder.insert_field(field_type=aw.fields.FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.insert_next_number = True
field_seq.update()
self.assertEqual(' SEQ  MySequence \\n', field_seq.get_field_code())
self.assertEqual('2', field_seq.result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SEQ.ResetNumbering.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSeq](../)

