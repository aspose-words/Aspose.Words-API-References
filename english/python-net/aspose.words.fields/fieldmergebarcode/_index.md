﻿---
title: FieldMergeBarcode class
linktitle: FieldMergeBarcode class
articleTitle: FieldMergeBarcode class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldMergeBarcode class. Implements the MERGEBARCODE field"
type: docs
weight: 680
url: /python-net/aspose.words.fields/fieldmergebarcode/
---

## FieldMergeBarcode class

Implements the MERGEBARCODE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Mail merge a barcode.


**Inheritance:** [FieldMergeBarcode](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldMergeBarcode()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [add_start_stop_char](./add_start_stop_char/) | Gets or sets whether to add Start/Stop characters for barcode types NW7 and CODE39. |
| [background_color](./background_color/) | Gets or sets the background color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF] |
| [barcode_type](./barcode_type/) | Gets or sets the barcode type (QR, etc.) |
| [barcode_value](./barcode_value/) | Gets or sets the barcode value. |
| [case_code_style](./case_code_style/) | Gets or sets the style of a Case Code for barcode type ITF14. The valid values are [STD|EXT|ADD] |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [display_text](./display_text/) | Gets or sets whether to display barcode data (text) along with image. |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [error_correction_level](./error_correction_level/) | Gets or sets an error correction level of QR Code. Valid values are [0, 3]. |
| [fix_check_digit](./fix_check_digit/) | Gets or sets whether to fix the check digit if it’s invalid. |
| [foreground_color](./foreground_color/) | Gets or sets the foreground color of the barcode symbol. Valid values are in the range [0, 0xFFFFFF] |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [pos_code_style](./pos_code_style/) | Gets or sets the style of a Point of Sale barcode (barcode types UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE]. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [scaling_factor](./scaling_factor/) | Gets or sets a scaling factor for the symbol. The value is in whole percentage points and the valid values are [10, 1000] |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [symbol_height](./symbol_height/) | Gets or sets the height of the symbol. The units are in TWIPS (1/1440 inch). |
| [symbol_rotation](./symbol_rotation/) | Gets or sets the rotation of the barcode symbol. Valid values are [0, 3] |
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

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

