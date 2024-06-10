---
title: FieldRD class
linktitle: FieldRD class
articleTitle: FieldRD class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldRD class. Implements the RD field"
type: docs
weight: 860
url: /python-net/aspose.words.fields/fieldrd/
---

## FieldRD class

Implements the RD field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Identifies a file to include when you create a table of contents, a table of authorities, or an index
with the TOC, TOA, or INDEX field


**Inheritance:** [FieldRD](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldRD()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [file_name](./file_name/) | Gets or sets the name of the file to include when generating a table of contents, table of authorities, or index. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [is_path_relative](./is_path_relative/) | Gets or sets whether the path is relative to the current document. |
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

Shows to use the RD field to create a table of contents entries from headings in other documents.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# Use a document builder to insert a table of contents,
# and then add one entry for the table of contents on the following page.
builder.insert_field(aw.fields.FieldType.FIELD_TOC, True)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.current_paragraph.paragraph_format.style_name = 'Heading 1'
builder.writeln('TOC entry from within this document')
# Insert an RD field, which references another local file system document in its FileName property.
# The TOC will also now accept all headings from the referenced document as entries for its table.
field = builder.insert_field(aw.fields.FieldType.FIELD_REF_DOC, True).as_field_rd()
field.file_name = ARTIFACTS_DIR + 'ReferencedDocument.docx'
self.assertEqual(' RD  {ArtifactsDir.Replace(@"\\",@"\\\\")}ReferencedDocument.docx', field.get_field_code())
# Create the document that the RD field is referencing and insert a heading.
# This heading will show up as an entry in the TOC field in our first document.
referenced_doc = aw.Document()
ref_doc_builder = aw.DocumentBuilder(referenced_doc)
ref_doc_builder.current_paragraph.paragraph_format.style_name = 'Heading 1'
ref_doc_builder.writeln('TOC entry from referenced document')
referenced_doc.save(ARTIFACTS_DIR + 'ReferencedDocument.docx')
doc.update_fields()
doc.save(ARTIFACTS_DIR + 'Field.field_rd.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

