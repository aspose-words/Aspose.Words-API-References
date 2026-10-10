---
title: FieldSeq class
linktitle: FieldSeq class
articleTitle: FieldSeq class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldSeq class. Implements the SEQ field"
type: docs
weight: 930
url: /ar/python-net/aspose.words.fields/fieldseq/
---

## FieldSeq class

Implements the SEQ field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Sequentially numbers chapters, tables, figures, and other user-defined lists of items in a document.


**Inheritance:** [FieldSeq](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldSeq()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [insert_next_number](./insert_next_number/) | Gets or sets whether to insert the next sequence number for the specified item. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [reset_heading_level](./reset_heading_level/) | Gets or sets an integer number representing a heading level to reset the sequence number to. Returns -1 if the number is absent. |
| [reset_number](./reset_number/) | Gets or sets an integer number to reset the sequence number to. Returns -1 if the number is absent. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [sequence_identifier](./sequence_identifier/) | Gets or sets the name assigned to the series of items that are to be numbered. |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

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

Shows how to combine table of contents and sequence fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# يمكن لحقل TOC إنشاء إدخال في جدول المحتويات لكل حقل SEQ موجود في المستند.
# كل إدخال يحتوي على الفقرة التي تحتوي على حقل SEQ،
# والرقم الصفحة التي يظهر فيها الحقل.
field_toc = builder.insert_field(field_type=FieldType.FIELD_TOC, update_field=True).as_field_toc()
# قم بتكوين حقل الفهرس هذا ليحتوي على خاصية SequenceIdentifier بقيمة "MySequence".
field_toc.table_of_figures_label = 'MySequence'
# قم بتكوين حقل الفهرس هذا ليلتقط فقط حقول SEQ التي تقع ضمن حدود إشارة مرجعية
# المسمى "TOCBookmark".
field_toc.bookmark_name = 'TOCBookmark'
builder.insert_break(aw.BreakType.PAGE_BREAK)
self.assertEqual(' TOC  \\c MySequence \\b TOCBookmark', field_toc.get_field_code())
# حقول SEQ تعرض عدًّا يزداد عند كل حقل SEQ.
# هذه الحقول تحافظ أيضًا على عدادات منفصلة لكل تسلسل مسمى فريد
# محددة بواسطة خاصية "SequenceIdentifier" لحقل SEQ.
# أدرج حقل SEQ يحتوي على معرف تسلسل يطابق خاصية TOC.
# خاصية TableOfFiguresLabel. هذا الحقل لن ينشئ إدخالًا في الفهرس لأنه خارج
# حدود الإشارة المرجعية المحددة بـ "BookmarkName".
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will not show up in the TOC because it is outside of the bookmark.')
builder.start_bookmark('TOCBookmark')
# تطابق تسلسل حقل SEQ الخاص بهذه الخاصية "TableOfFiguresLabel" في الفهرس وهو ضمن حدود الإشارة المرجعية.
# ستظهر الفقرة التي تحتوي على هذا الحقل في الفهرس كإدخال.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will show up in the TOC next to the entry for the above caption.')
# تسلسل حقل SEQ هذا لا يطابق خاصية الفهرس "TableOfFiguresLabel"،
# وهو ضمن حدود الإشارة المرجعية. فقرتها لن تظهر في الفهرس كإدخال.
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'OtherSequence'
builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.")
# تطابق تسلسل حقل SEQ هذا خاصية الفهرس "TableOfFiguresLabel" وهو ضمن حدود الإشارة المرجعية.
# هذا الحقل يشير أيضًا إلى إشارة مرجعية أخرى. محتويات تلك الإشارة ستظهر في إدخال الفهرس لهذا الحقل SEQ.
# حقل SEQ نفسه لن يعرض محتويات تلك الإشارة المرجعية.
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.bookmark_name = 'SEQBookmark'
self.assertEqual(' SEQ  MySequence SEQBookmark', field_seq.get_field_code())
# أنشئ إشارة مرجعية بمحتويات ستظهر في إدخال الفهرس بسبب إشارة حقل SEQ أعلاه إليها.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('SEQBookmark')
builder.write('MySequence #')
field_seq = builder.insert_field(field_type=FieldType.FIELD_SEQUENCE, update_field=True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', text from inside SEQBookmark.')
builder.end_bookmark('SEQBookmark')
builder.end_bookmark('TOCBookmark')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SEQ.Bookmark.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

