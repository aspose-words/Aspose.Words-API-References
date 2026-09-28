---
title: FieldRef.include_note_or_comment property
linktitle: include_note_or_comment property
articleTitle: include_note_or_comment property
second_title: Aspose.Words for Python
description: "FieldRef.include_note_or_comment property. Gets or sets whether to increment footnote, endnote, and annotation numbers that are marked by the bookmark, and insert the corresponding footnote, endnote, and comment text."
type: docs
weight: 30
url: /zh/python-net/aspose.words.fields/fieldref/include_note_or_comment/
---

## FieldRef.include_note_or_comment property

Gets or sets whether to increment footnote, endnote, and annotation numbers that are
marked by the bookmark, and insert the corresponding footnote, endnote, and comment text.


```python
@property
def include_note_or_comment(self) -> bool:
    ...

@include_note_or_comment.setter
def include_note_or_comment(self, value: bool):
    ...

```

### Examples

Shows how to insert REF fields to reference bookmarks.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_bookmark('MyBookmark')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='MyBookmark footnote #1')
builder.write('Text that will appear in REF field')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='MyBookmark footnote #2')
builder.end_bookmark('MyBookmark')
builder.move_to_document_start()
# 我们将应用自定义列表格式，其中尖括号的数量指示当前所在的列表层级。
builder.list_format.apply_number_default()
builder.list_format.list_level.number_format = '> \x00'
# 插入一个 REF 字段，其中包含我们书签内的文本，充当超链接，并复制书签的脚注。
field = ExField._insert_field_ref(builder, 'MyBookmark', '', '\n')
field.include_note_or_comment = True
field.insert_hyperlink = True
self.assertEqual(' REF  MyBookmark \\f \\h', field.get_field_code())
# 插入一个 REF 字段，并显示引用的书签是在其上方还是下方。
field = ExField._insert_field_ref(builder, 'MyBookmark', 'The referenced paragraph is ', ' this field.\n')
field.insert_relative_position = True
self.assertEqual(' REF  MyBookmark \\p', field.get_field_code())
# 显示书签在文档中出现的列表编号。
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's paragraph number is ", '\n')
field.insert_paragraph_number = True
self.assertEqual(' REF  MyBookmark \\n', field.get_field_code())
# 显示书签的列表编号，但省略非分隔符字符，例如尖括号。
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's paragraph number, non-delimiters suppressed, is ", '\n')
field.insert_paragraph_number = True
field.suppress_non_delimiters = True
self.assertEqual(' REF  MyBookmark \\n \\t', field.get_field_code())
# 向下移动一个列表层级。
builder.list_format.list_level_number += 1
builder.list_format.list_level.number_format = '>> \x01'
# 显示书签的列表编号以及其上方所有列表层级的编号。
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's full context paragraph number is ", '\n')
field.insert_paragraph_number_in_full_context = True
self.assertEqual(' REF  MyBookmark \\w', field.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# 显示此 REF 字段与其引用的书签之间的列表层级编号。
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's relative paragraph number is ", '\n')
field.insert_paragraph_number_in_relative_context = True
self.assertEqual(' REF  MyBookmark \\r', field.get_field_code())
# 在文档末尾，书签将显示为此处的列表项。
builder.writeln('List level above bookmark')
builder.list_format.list_level_number += 1
builder.list_format.list_level.number_format = '>>> \x02'
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.REF.docx')
```

Shows how to insert REF fields to reference bookmarks (InsertFieldRef).

```python
@staticmethod
def _insert_field_ref(builder, bookmark_name, text_before, text_after):
    builder.write(text_before)
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_REF, update_field=True).as_field_ref()
    field.bookmark_name = bookmark_name
    builder.write(text_after)
    return field
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldRef](../)

