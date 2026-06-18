---
title: FieldRef.number_separator property
linktitle: number_separator property
articleTitle: number_separator property
second_title: Aspose.Words for Python
description: "FieldRef.number_separator property. Gets or sets the character sequence that is used to separate sequence numbers and page numbers."
type: docs
weight: 90
url: /python-net/aspose.words.fields/fieldref/number_separator/
---

## FieldRef.number_separator property

Gets or sets the character sequence that is used to separate sequence numbers and page numbers.


```python
@property
def number_separator(self) -> str:
    ...

@number_separator.setter
def number_separator(self, value: str):
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
# We will apply a custom list format, where the amount of angle brackets indicates the list level we are currently at.
builder.list_format.apply_number_default()
builder.list_format.list_level.number_format = '> \x00'
# Insert a REF field that will contain the text within our bookmark, act as a hyperlink, and clone the bookmark's footnotes.
field = ExField._insert_field_ref(builder, 'MyBookmark', '', '\n')
field.include_note_or_comment = True
field.insert_hyperlink = True
self.assertEqual(' REF  MyBookmark \\f \\h', field.get_field_code())
# Insert a REF field, and display whether the referenced bookmark is above or below it.
field = ExField._insert_field_ref(builder, 'MyBookmark', 'The referenced paragraph is ', ' this field.\n')
field.insert_relative_position = True
self.assertEqual(' REF  MyBookmark \\p', field.get_field_code())
# Display the list number of the bookmark as it appears in the document.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's paragraph number is ", '\n')
field.insert_paragraph_number = True
self.assertEqual(' REF  MyBookmark \\n', field.get_field_code())
# Display the bookmark's list number, but with non-delimiter characters, such as the angle brackets, omitted.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's paragraph number, non-delimiters suppressed, is ", '\n')
field.insert_paragraph_number = True
field.suppress_non_delimiters = True
self.assertEqual(' REF  MyBookmark \\n \\t', field.get_field_code())
# Move down one list level.
builder.list_format.list_level_number += 1
builder.list_format.list_level.number_format = '>> \x01'
# Display the list number of the bookmark and the numbers of all the list levels above it.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's full context paragraph number is ", '\n')
field.insert_paragraph_number_in_full_context = True
self.assertEqual(' REF  MyBookmark \\w', field.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Display the list level numbers between this REF field, and the bookmark that it is referencing.
field = ExField._insert_field_ref(builder, 'MyBookmark', "The bookmark's relative paragraph number is ", '\n')
field.insert_paragraph_number_in_relative_context = True
self.assertEqual(' REF  MyBookmark \\r', field.get_field_code())
# At the end of the document, the bookmark will show up as a list item here.
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

