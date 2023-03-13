﻿---
title: FieldBarcode class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the BARCODE field"
type: docs
weight: 170
url: /python-net/aspose.words.fields/fieldbarcode/
---

## FieldBarcode class

Implements the BARCODE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Inserts a postal barcode in a machine-readable form of address used by the U.S. Postal Service.


**Inheritance:** [FieldBarcode](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldBarcode()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [facing_identification_mark](./facing_identification_mark/) | Gets or sets the type of a Facing Identification Mark (FIM) to insert. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_bookmark](./is_bookmark/) | Gets or sets whether [FieldBarcode.postal_address](./postal_address/) is the name of a bookmark. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [is_us_postal_address](./is_us_postal_address/) | Gets or sets whether [FieldBarcode.postal_address](./postal_address/) is a U.S. postal address. |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [postal_address](./postal_address/) | Gets or sets the postal address used for generating a barcode or the name of the bookmark that refers to it. |
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

Shows how to use the BARCODE field to display U.S. ZIP codes in the form of a barcode.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln()

# Below are two ways of using BARCODE fields to display custom values as barcodes.
# 1 -  Store the value that the barcode will display in the postal_address property:
field = builder.insert_field(aw.fields.FieldType.FIELD_BARCODE, True).as_field_barcode()

# This value needs to be a valid ZIP code.
field.postal_address = "96801"
field.is_us_postal_address = True
field.facing_identification_mark = "C"

self.assertEqual(" BARCODE  96801 \\u \\f C", field.get_field_code())

builder.insert_break(aw.BreakType.LINE_BREAK)

# 2 -  Reference a bookmark that stores the value that this barcode will display:
field = builder.insert_field(aw.fields.FieldType.FIELD_BARCODE, True).as_field_barcode()
field.postal_address = "BarcodeBookmark"
field.is_bookmark = True

self.assertEqual(" BARCODE  BarcodeBookmark \\b", field.get_field_code())

# The bookmark that the BARCODE field references in its "postal_address" property
# need to contain nothing besides the valid ZIP code.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark("BarcodeBookmark")
builder.writeln("968877")
builder.end_bookmark("BarcodeBookmark")

doc.save(ARTIFACTS_DIR + "Field.field_barcode.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

