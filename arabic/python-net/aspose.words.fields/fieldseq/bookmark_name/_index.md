---
title: FieldSeq.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldSeq.bookmark_name property. Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location."
type: docs
weight: 20
url: /ar/python-net/aspose.words.fields/fieldseq/bookmark_name/
---

## FieldSeq.bookmark_name property

Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location.


```python
@property
def bookmark_name(self) -> str:
    ...

@bookmark_name.setter
def bookmark_name(self, value: str):
    ...

```

### Examples

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

* module [aspose.words.fields](../../)
* class [FieldSeq](../)

