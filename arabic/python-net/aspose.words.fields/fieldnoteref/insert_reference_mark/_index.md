---
title: FieldNoteRef.insert_reference_mark property
linktitle: insert_reference_mark property
articleTitle: insert_reference_mark property
second_title: Aspose.Words for Python
description: "FieldNoteRef.insert_reference_mark property. Inserts the reference mark with the same character formatting as the Footnote Reference or Endnote Reference style."
type: docs
weight: 40
url: /ar/python-net/aspose.words.fields/fieldnoteref/insert_reference_mark/
---

## FieldNoteRef.insert_reference_mark property

Inserts the reference mark with the same character formatting as the Footnote Reference
or Endnote Reference style.


```python
@property
def insert_reference_mark(self) -> bool:
    ...

@insert_reference_mark.setter
def insert_reference_mark(self, value: bool):
    ...

```

### Examples

Shows to insert NOTEREF fields, and modify their appearance.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أنشئ علامة مرجعية مع حاشية سفلية سيشير إليها حقل NOTEREF.
ExField._insert_bookmark_with_footnote(builder, 'MyBookmark1', 'Contents of MyBookmark1', 'Footnote from MyBookmark1')
# سيعرض حقل NOTEREF هذا رقم الحاشية السفلية داخل العلامة المرجعية المشار إليها.
# يتيح تعيين خاصية InsertHyperlink القفز إلى العلامة المرجعية عبر الضغط على Ctrl + النقر على الحقل في Microsoft Word.
self.assertEqual(' NOTEREF  MyBookmark2 \\h', ExField._insert_field_note_ref(builder, 'MyBookmark2', True, False, False, 'Hyperlink to Bookmark2, with footnote number ').get_field_code())
# عند استخدام العلامة \p، بعد رقم الحاشية السفلية، يعرض الحقل أيضًا موضع العلامة المرجعية بالنسبة للحقل.
# العلامة المرجعية Bookmark1 فوق هذا الحقل وتحتوي على رقم الحاشية السفلية 1، لذا سيكون الناتج "1 above" عند التحديث.
self.assertEqual(' NOTEREF  MyBookmark1 \\h \\p', ExField._insert_field_note_ref(builder, 'MyBookmark1', True, True, False, 'Bookmark1, with footnote number ').get_field_code())
# العلامة المرجعية Bookmark2 تحت هذا الحقل وتحتوي على رقم الحاشية السفلية 2، لذا سيعرض الحقل "2 below".
# تجعل العلامة \f الرقم 2 يظهر بنفس تنسيق تسمية رقم الحاشية السفلية في النص الفعلي.
self.assertEqual(' NOTEREF  MyBookmark2 \\h \\p \\f', ExField._insert_field_note_ref(builder, 'MyBookmark2', True, True, True, 'Bookmark2, with footnote number ').get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
ExField._insert_bookmark_with_footnote(builder, 'MyBookmark2', 'Contents of MyBookmark2', 'Footnote from MyBookmark2')
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.NOTEREF.docx')
```

Shows to insert NOTEREF fields, and modify their appearance (InsertFieldNoteRef).

```python
@staticmethod
def _insert_field_note_ref(builder, bookmark_name, insert_hyperlink, insert_relative_position, insert_reference_mark, text_before):
    builder.write(text_before)
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_NOTE_REF, update_field=True).as_field_note_ref()
    field.bookmark_name = bookmark_name
    field.insert_hyperlink = insert_hyperlink
    field.insert_relative_position = insert_relative_position
    field.insert_reference_mark = insert_reference_mark
    builder.writeln()
    return field

@staticmethod
def _insert_bookmark_with_footnote(builder, bookmark_name, bookmark_text, footnote_text):
    builder.start_bookmark(bookmark_name)
    builder.write(bookmark_text)
    builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text=footnote_text)
    builder.end_bookmark(bookmark_name)
    builder.writeln()
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldNoteRef](../)

