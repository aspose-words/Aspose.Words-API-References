﻿---
title: FieldUserInitials class
linktitle: FieldUserInitials class
articleTitle: FieldUserInitials class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldUserInitials class. Implements the USERINITIALS field"
type: docs
weight: 1130
url: /python-net/aspose.words.fields/fielduserinitials/
---

## FieldUserInitials class

Implements the USERINITIALS field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Retrieves the current user's initials.


**Inheritance:** [FieldUserInitials](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldUserInitials()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |
| [user_initials](./user_initials/) | Gets or sets the current user's initials. |

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

Shows how to use the USERINITIALS field.

```python
doc = aw.Document()
# Create a UserInformation object and set it as the source of user information for any fields that we create.
user_information = aw.fields.UserInformation()
user_information.initials = 'J. D.'
doc.field_options.current_user = user_information
# Create a USERINITIALS field to display the current user's initials,
# taken from the UserInformation object we created above.
builder = aw.DocumentBuilder(doc=doc)
field_user_initials = builder.insert_field(field_type=aw.fields.FieldType.FIELD_USER_INITIALS, update_field=True).as_field_user_initials()
self.assertEqual(user_information.initials, field_user_initials.result)
self.assertEqual(' USERINITIALS ', field_user_initials.get_field_code())
self.assertEqual('J. D.', field_user_initials.result)
# We can set this property to get our field to override the value currently stored in the UserInformation object.
field_user_initials.user_initials = 'J. C.'
field_user_initials.update()
self.assertEqual(' USERINITIALS  "J. C."', field_user_initials.get_field_code())
self.assertEqual('J. C.', field_user_initials.result)
# This does not affect the value in the UserInformation object.
self.assertEqual('J. D.', doc.field_options.current_user.initials)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.USERINITIALS.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

