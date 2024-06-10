---
title: FieldSeq.bookmark_name property
linktitle: bookmark_name property
articleTitle: bookmark_name property
second_title: Aspose.Words for Python
description: "FieldSeq.bookmark_name property. Gets or sets a bookmark name that refers to an item elsewhere in the document rather than in the current location."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldseq/bookmark_name/
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
builder = aw.DocumentBuilder(doc)
# A TOC field can create an entry in its table of contents for each SEQ field found in the document.
# Each entry contains the paragraph that contains the SEQ field,
# and the number of the page that the field appears on.
field_toc = builder.insert_field(aw.fields.FieldType.FIELD_TOC, True).as_field_toc()
# Configure this TOC field to have a "sequence_identifier" property with a value of "MySequence".
field_toc.table_of_figures_label = 'MySequence'
# Configure this TOC field to only pick up SEQ fields that are within the bounds of a bookmark
# named "TOCBookmark".
field_toc.bookmark_name = 'TOCBookmark'
builder.insert_break(aw.BreakType.PAGE_BREAK)
self.assertEqual(' TOC  \\c MySequence \\b TOCBookmark', field_toc.get_field_code())
# SEQ fields display a count that increments at each SEQ field.
# These fields also maintain separate counts for each unique named sequence
# identified by the SEQ field's "sequence_identifier" property.
# Insert a SEQ field that has a sequence identifier that matches the TOC's
# "table_of_figures_label" property. This field will not create an entry in the TOC since it is outside
# the bookmark's bounds designated by "BookmarkName".
builder.write('MySequence #')
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will not show up in the TOC because it is outside of the bookmark.')
builder.start_bookmark('TOCBookmark')
# This SEQ field's sequence matches the TOC's "table_of_figures_label" property and is within the bookmark's bounds.
# The paragraph that contains this field will show up in the TOC as an entry.
builder.write('MySequence #')
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', will show up in the TOC next to the entry for the above caption.')
# This SEQ field's sequence does not match the TOC's "table_of_figures_label" property,
# and is within the bounds of the bookmark. Its paragraph will not show up in the TOC as an entry.
builder.write('MySequence #')
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = 'OtherSequence'
builder.writeln(", will not show up in the TOC because it's from a different sequence identifier.")
# This SEQ field's sequence matches the TOC's "table_of_figures_label" property and is within the bounds of the bookmark.
# This field also references another bookmark. The contents of that bookmark will appear in the TOC entry for this SEQ field.
# The SEQ field itself will not display the contents of that bookmark.
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
field_seq.bookmark_name = 'SEQBookmark'
self.assertEqual(' SEQ  MySequence SEQBookmark', field_seq.get_field_code())
# Create a bookmark with contents that will show up in the TOC entry due to the above SEQ field referencing it.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('SEQBookmark')
builder.write('MySequence #')
field_seq = builder.insert_field(aw.fields.FieldType.FIELD_SEQUENCE, True).as_field_seq()
field_seq.sequence_identifier = 'MySequence'
builder.writeln(', text from inside SEQBookmark.')
builder.end_bookmark('SEQBookmark')
builder.end_bookmark('TOCBookmark')
doc.update_fields()
doc.save(ARTIFACTS_DIR + 'Field.toc_seq_bookmark.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldSeq](../)

