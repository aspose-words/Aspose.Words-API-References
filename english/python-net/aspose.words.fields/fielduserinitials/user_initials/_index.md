---
title: FieldUserInitials.user_initials property
linktitle: user_initials property
articleTitle: user_initials property
second_title: Aspose.Words for Python
description: "FieldUserInitials.user_initials property. Gets or sets the current user's initials."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fielduserinitials/user_initials/
---

## FieldUserInitials.user_initials property

Gets or sets the current user's initials.


```python
@property
def user_initials(self) -> str:
    ...

@user_initials.setter
def user_initials(self, value: str):
    ...

```

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

* module [aspose.words.fields](../../)
* class [FieldUserInitials](../)

