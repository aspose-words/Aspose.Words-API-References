---
title: FieldNoteRef class
linktitle: FieldNoteRef class
articleTitle: FieldNoteRef class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldNoteRef class. Implements the NOTEREF field"
type: docs
weight: 740
url: /python-net/aspose.words.fields/fieldnoteref/
---

## FieldNoteRef class

Implements the NOTEREF field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Inserts the mark of the footnote or endnote that is marked by the specified bookmark.


**Inheritance:** [FieldNoteRef](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldNoteRef()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets the name of the bookmark. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [insert_hyperlink](./insert_hyperlink/) | Gets or sets whether to insert a hyperlink to the bookmarked paragraph. |
| [insert_reference_mark](./insert_reference_mark/) | Inserts the reference mark with the same character formatting as the Footnote Reference or Endnote Reference style. |
| [insert_relative_position](./insert_relative_position/) | Gets or sets whether to insert a relative position of the bookmarked paragraph. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
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

Shows how to cross-reference footnotes with the NOTEREF field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('CrossReference: ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_NOTE_REF, update_field=False).as_field_note_ref()  # <--- don't update field
field.bookmark_name = 'CrossRefBookmark'
field.insert_hyperlink = True
field.insert_reference_mark = True
field.insert_relative_position = False
builder.writeln()
builder.start_bookmark('CrossRefBookmark')
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Cross referenced footnote.')
builder.end_bookmark('CrossRefBookmark')
builder.writeln()
doc.update_fields()
# This field works only in older versions of Microsoft Word.
doc.save(file_name=ARTIFACTS_DIR + 'Field.NOTEREF.doc')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

