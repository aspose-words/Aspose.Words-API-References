---
title: default_user property
second_title: Aspose.Words for Python via .NET API Reference
description: "Default user information."
type: docs
weight: 30
url: /python-net/aspose.words.fields/userinformation/default_user/
---

## UserInformation.default_user property

Default user information.

Use the [FieldOptions.current_user](../../fieldoptions/current_user/) property to specify user information for single document.



### Examples

Shows how to set user details, and display them using fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Create a UserInformation object and set it as the data source for fields that display user information.
user_information = aw.fields.UserInformation()
user_information.name = "John Doe"
user_information.initials = "J. D."
user_information.address = "123 Main Street"

doc.field_options.current_user = user_information

# Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
# the respective properties of the UserInformation object that we have created above.
self.assertEqual(user_information.name, builder.insert_field(" USERNAME ").result)
self.assertEqual(user_information.initials, builder.insert_field(" USERINITIALS ").result)
self.assertEqual(user_information.address, builder.insert_field(" USERADDRESS ").result)

# The field options object also has a static default user that fields from all documents can refer to.
user_information.default_user.name = "Default User"
user_information.default_user.initials = "D. U."
user_information.default_user.address = "One Microsoft Way"
doc.field_options.current_user = aw.fields.UserInformation.default_user

self.assertEqual("Default User", builder.insert_field(" USERNAME ").result)
self.assertEqual("D. U.", builder.insert_field(" USERINITIALS ").result)
self.assertEqual("One Microsoft Way", builder.insert_field(" USERADDRESS ").result)

doc.update_fields()
doc.save(ARTIFACTS_DIR + "FieldOptions.current_user.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [UserInformation](../)

