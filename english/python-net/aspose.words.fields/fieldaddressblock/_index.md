---
title: FieldAddressBlock class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the ADDRESSBLOCK field."
type: docs
weight: 70
url: /python-net/aspose.words.fields/fieldaddressblock/
---

## FieldAddressBlock class

Implements the ADDRESSBLOCK field.


Represents an address block. An *address block* is a block of text specifying information
appropriate for a postal mailing address, in the order required by the destination country.



**Inheritance:** [FieldAddressBlock](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldAddressBlock()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [excluded_country_or_region_name](./excluded_country_or_region_name/) | Gets or sets the excluded country/region name. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [format_address_on_country_or_region](./format_address_on_country_or_region/) | Gets or sets whether to format the address according to the country/region of the recipient as defined by POST\*CODE (Universal Postal Union 2006). |
| [include_country_or_region_name](./include_country_or_region_name/) | Gets or sets whether to include the name of the country/region. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [language_id](./language_id/) | Gets or sets the language ID used to format the address. |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [name_and_address_format](./name_and_address_format/) | Gets or sets the name and address format. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be null.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ get_field_names()](./get_field_names/#default) | Returns a collection of mail merge field names used by the field. |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

### Examples

Shows how to get mail merge field names used by a field.

```python
doc = aw.Document(MY_DIR + "Field sample - ADDRESSBLOCK.docx")

address_fields_expect = [
    "Company", "First Name", "Middle Name", "Last Name", "Suffix", "Address 1", "City", "State",
    "Country or Region", "Postal Code"
    ]

address_block_field = doc.range.fields[0].as_field_address_block()
address_block_field_names = address_block_field.get_field_names()
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

