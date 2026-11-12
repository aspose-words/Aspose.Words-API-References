---
title: FieldRef.insert_relative_position property
linktitle: insert_relative_position property
articleTitle: insert_relative_position property
second_title: Aspose.Words for Python
description: "FieldRef.insert_relative_position property. Gets or sets whether to insert the relative position of the referenced paragraph."
type: docs
weight: 80
url: /ru/python-net/aspose.words.fields/fieldref/insert_relative_position/
---

## FieldRef.insert_relative_position property

Gets or sets whether to insert the relative position of the referenced paragraph.


```python
@property
def insert_relative_position(self) -> bool:
    ...

@insert_relative_position.setter
def insert_relative_position(self, value: bool):
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
# Мы применим пользовательский формат списка, где количество угловых скобок указывает текущий уровень списка.
builder.list_format.apply_number_default()
builder.list_format.list_level.number_format = '> \x00'
# Вставьте поле REF, которое будет содержать текст внутри нашей закладки, выступать в качестве гиперссылки и копировать сноски закладки.
field = ExField._insert_field_ref(builder, 'MyBookmark', '', '\n')
field.include_note_or_comment = True
field.insert_hyperlink = True
self.assertEqual(' REF  MyBookmark \\f \\h', field.get_field_code())
# Вставьте поле REF и отобразите, находится ли ссылка на закладку выше или ниже него.
field = ExField._insert_field_ref(builder, 'MyBookmark', 'The referenced paragraph is ', ' this field.\n')
field.insert_relative_position = True
self.assertEqual(' REF  MyBookmark \\p', field.get_field_code())
# Отобразите номер списка закладки так, как он появляется в документе.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's paragraph number is ", '\n')
field.insert_paragraph_number = True
self.assertEqual(' REF  MyBookmark \\n', field.get_field_code())
# Отобразите номер списка закладки, но без символов-разделителей, таких как угловые скобки.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's paragraph number, non-delimiters suppressed, is ", '\n')
field.insert_paragraph_number = True
field.suppress_non_delimiters = True
self.assertEqual(' REF  MyBookmark \\n \\t', field.get_field_code())
# Перейдите на один уровень ниже в списке.
builder.list_format.list_level_number += 1
builder.list_format.list_level.number_format = '>> \x01'
# Отобразите номер списка закладки и номера всех уровней списка выше неё.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's full context paragraph number is ", '\n')
field.insert_paragraph_number_in_full_context = True
self.assertEqual(' REF  MyBookmark \\w', field.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Отобразите номера уровней списка между этим полем REF и закладкой, на которую оно ссылается.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's relative paragraph number is ", '\n')
field.insert_paragraph_number_in_relative_context = True
self.assertEqual(' REF  MyBookmark \\r', field.get_field_code())
# В конце документа закладка появится здесь как элемент списка.
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

