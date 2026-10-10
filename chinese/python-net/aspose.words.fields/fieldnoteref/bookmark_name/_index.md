---
title: FieldNoteRef.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldNoteRef.bookmark_name property. Gets or sets the name of the bookmark."
type: docs
weight: 20
url: /zh/python-net/aspose.words.fields/fieldnoteref/bookmark_name/
---

## FieldNoteRef.bookmark_name property

Gets or sets the name of the bookmark.


```python
@property
def bookmark_name(self) -> str:
    ...

@bookmark_name.setter
def bookmark_name(self, value: str):
    ...

```

### Examples

Shows to insert NOTEREF fields, and modify their appearance.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 创建一个带有脚注的书签，供 NOTEREF 字段引用。
ExField._insert_bookmark_with_footnote(builder, 'MyBookmark1', 'Contents of MyBookmark1', 'Footnote from MyBookmark1')
# 此 NOTEREF 字段将显示引用书签内脚注的编号。
# 设置 InsertHyperlink 属性可让我们在 Microsoft Word 中通过 Ctrl + 单击字段跳转到书签。
self.assertEqual(' NOTEREF  MyBookmark2 \\h', ExField._insert_field_note_ref(builder, 'MyBookmark2', True, False, False, 'Hyperlink to Bookmark2, with footnote number ').get_field_code())
# 使用 \\p 标志时，在脚注编号之后，字段还会显示书签相对于字段的位置。
# Bookmark1 位于此字段上方并包含脚注编号 1，因此更新后结果将是 \"1 above\"。
self.assertEqual(' NOTEREF  MyBookmark1 \\h \\p', ExField._insert_field_note_ref(builder, 'MyBookmark1', True, True, False, 'Bookmark1, with footnote number ').get_field_code())
# Bookmark2 位于此字段下方并包含脚注编号 2，因此字段将显示 \"2 below\"。
# \\f 标志使数字 2 以与实际文本中脚注编号标签相同的格式出现。
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

