﻿---
title: FieldInclude class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the INCLUDE field"
type: docs
weight: 570
url: /python-net/aspose.words.fields/fieldinclude/
---

## FieldInclude class

Implements the INCLUDE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Inserts all or part of the text and graphics contained in another document.


**Inheritance:** [FieldInclude](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldInclude()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets the name of the bookmark in the document to include. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [lock_fields](./lock_fields/) | Gets or sets whether to prevent fields in the included document from being updated. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [source_full_name](./source_full_name/) | Gets or sets the location of the document. |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [text_converter](./text_converter/) | Gets or sets the name of the text converter for the format of the included file. |
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

Shows how to create an INCLUDE field, and set its properties.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# We can use an INCLUDE field to import a portion of another document in the local file system.
# The bookmark from the other document that we reference with this field contains this imported portion.
field = builder.insert_field(aw.fields.FieldType.FIELD_INCLUDE, True).as_field_include()
field.source_full_name = MY_DIR + "Bookmarks.docx"
field.bookmark_name = "MyBookmark1"
field.lock_fields = False
field.text_converter = "Microsoft Word"

self.assertRegex(field.get_field_code(), r' INCLUDE .* MyBookmark1 \\c "Microsoft Word"')

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_include.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

