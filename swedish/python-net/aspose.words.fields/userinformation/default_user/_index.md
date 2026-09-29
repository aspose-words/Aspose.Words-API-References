---
title: UserInformation.default_user property
linktitle: default_user property
articleTitle: default_user property
second_title: Aspose.Words for Python
description: "UserInformation.default_user property. Default user information."
type: docs
weight: 30
url: /sv/python-net/aspose.words.fields/userinformation/default_user/
---

## UserInformation.default_user property

Default user information.


```python
@property
def default_user(self) -> aspose.words.fields.UserInformation:
    ...

```

### Remarks

Use the [FieldOptions.current_user](../../fieldoptions/current_user/) property to specify user information for single document.



### Examples

Shows how to set user details, and display them using fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Skapa ett UserInformation-objekt och ange det som datakälla för fält som visar användarinformation.
user_information = aw.fields.UserInformation()
user_information.name = 'John Doe'
user_information.initials = 'J. D.'
user_information.address = '123 Main Street'
doc.field_options.current_user = user_information
# Infoga fälten USERNAME, USERINITIALS och USERADDRESS, som visar värden av
# de respektive egenskaperna i UserInformation-objektet som vi skapade ovan.
self.assertEqual(user_information.name, builder.insert_field(field_code=' USERNAME ').result)
self.assertEqual(user_information.initials, builder.insert_field(field_code=' USERINITIALS ').result)
self.assertEqual(user_information.address, builder.insert_field(field_code=' USERADDRESS ').result)
# Fältalternativobjektet har också en statisk standardanvändare som fält från alla dokument kan referera till.
aw.fields.UserInformation.default_user.name = 'Default User'
aw.fields.UserInformation.default_user.initials = 'D. U.'
aw.fields.UserInformation.default_user.address = 'One Microsoft Way'
doc.field_options.current_user = aw.fields.UserInformation.default_user
self.assertEqual('Default User', builder.insert_field(field_code=' USERNAME ').result)
self.assertEqual('D. U.', builder.insert_field(field_code=' USERINITIALS ').result)
self.assertEqual('One Microsoft Way', builder.insert_field(field_code=' USERADDRESS ').result)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'FieldOptions.CurrentUser.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [UserInformation](../)

