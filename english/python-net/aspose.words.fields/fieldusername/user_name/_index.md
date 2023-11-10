---
title: FieldUserName.user_name property
linktitle: user_name property
articleTitle: user_name property
second_title: Aspose.Words for Python
description: "FieldUserName.user_name property. Gest or sets the current user's name."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldusername/user_name/
---

## FieldUserName.user_name property

Gest or sets the current user's name.


```python
@property
def user_name(self) -> str:
    ...

@user_name.setter
def user_name(self, value: str):
    ...

```

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

* module [aspose.words.fields](../../)
* class [FieldUserName](../)

