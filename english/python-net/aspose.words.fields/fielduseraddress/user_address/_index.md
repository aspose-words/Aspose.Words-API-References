---
title: FieldUserAddress.user_address property
linktitle: user_address property
articleTitle: user_address property
second_title: Aspose.Words for Python
description: "FieldUserAddress.user_address property. Gets or sets the current user's postal address."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fielduseraddress/user_address/
---

## FieldUserAddress.user_address property

Gets or sets the current user's postal address.


```python
@property
def user_address(self) -> str:
    ...

@user_address.setter
def user_address(self, value: str):
    ...

```

### Examples

Shows how to use the USERADDRESS field.

```python
doc = aw.Document()
# Create a UserInformation object and set it as the source of user information for any fields that we create.
user_information = aw.fields.UserInformation()
user_information.address = '123 Main Street'
doc.field_options.current_user = user_information
# Create a USERADDRESS field to display the current user's address,
# taken from the UserInformation object we created above.
builder = aw.DocumentBuilder(doc)
field_user_address = builder.insert_field(aw.fields.FieldType.FIELD_USER_ADDRESS, True).as_field_user_address()
self.assertEqual(' USERADDRESS ', field_user_address.get_field_code())
self.assertEqual('123 Main Street', field_user_address.result)
# We can set this property to get our field to override the value currently stored in the UserInformation object.
field_user_address.user_address = '456 North Road'
field_user_address.update()
self.assertEqual(' USERADDRESS  "456 North Road"', field_user_address.get_field_code())
self.assertEqual('456 North Road', field_user_address.result)
# This does not affect the value in the UserInformation object.
self.assertEqual('123 Main Street', doc.field_options.current_user.address)
doc.update_fields()
doc.save(ARTIFACTS_DIR + 'Field.field_user_address.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldUserAddress](../)

