﻿---
title: FieldUserName class
linktitle: FieldUserName class
articleTitle: FieldUserName class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldUserName class. Implements the USERNAME field"
type: docs
weight: 1140
url: /python-net/aspose.words.fields/fieldusername/
---

## FieldUserName class

Implements the USERNAME field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Retrieves the current user's name.


**Inheritance:** [FieldUserName](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldUserName()](./__init__/#default) | The default constructor. |

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
| [user_name](./user_name/) | Gest or sets the current user's name. |

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

Shows how to use the USERNAME field.

```python
doc = aw.Document()

# Create a UserInformation object and set it as the source of user information for any fields that we create.
user_information = aw.fields.UserInformation()
user_information.name = "John Doe"
doc.field_options.current_user = user_information

builder = aw.DocumentBuilder(doc)

# Create a USERNAME field to display the current user's name,
# taken from the UserInformation object we created above.
field_user_name = builder.insert_field(aw.fields.FieldType.FIELD_USER_NAME, True).as_field_user_name()
self.assertEqual(user_information.name, field_user_name.result)

self.assertEqual(" USERNAME ", field_user_name.get_field_code())
self.assertEqual("John Doe", field_user_name.result)

# We can set this property to get our field to override the value currently stored in the UserInformation object.
field_user_name.user_name = "Jane Doe"
field_user_name.update()

self.assertEqual(" USERNAME  \"Jane Doe\"", field_user_name.get_field_code())
self.assertEqual("Jane Doe", field_user_name.result)

# This does not affect the value in the UserInformation object.
self.assertEqual("John Doe", doc.field_options.current_user.name)

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_user_name.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

