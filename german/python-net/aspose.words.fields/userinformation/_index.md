---
title: UserInformation class
linktitle: UserInformation class
articleTitle: UserInformation class
second_title: Aspose.Words for Python
description: "aspose.words.fields.UserInformation class. Specifies information about the user"
type: docs
weight: 1330
url: /de/python-net/aspose.words.fields/userinformation/
---

## UserInformation class

Specifies information about the user.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [UserInformation()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [address](./address/) | Gets or sets the user's postal address. |
| [default_user](./default_user/) | Default user information. |
| [initials](./initials/) | Gets or sets the user's initials. |
| [name](./name/) | Gets or sets the user's name. |

### Examples

Shows how to set user details, and display them using fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Erstellen Sie ein UserInformation-Objekt und setzen Sie es als Datenquelle für Felder, die Benutzerinformationen anzeigen.
user_information = aw.fields.UserInformation()
user_information.name = 'John Doe'
user_information.initials = 'J. D.'
user_information.address = '123 Main Street'
doc.field_options.current_user = user_information
# Fügen Sie die Felder USERNAME, USERINITIALS und USERADDRESS ein, die Werte von
# den jeweiligen Eigenschaften des oben erstellten UserInformation-Objekts.
self.assertEqual(user_information.name, builder.insert_field(field_code=' USERNAME ').result)
self.assertEqual(user_information.initials, builder.insert_field(field_code=' USERINITIALS ').result)
self.assertEqual(user_information.address, builder.insert_field(field_code=' USERADDRESS ').result)
# Das Feldoptionen-Objekt hat außerdem einen statischen Standardbenutzer, auf den Felder aus allen Dokumenten verweisen können.
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

* module [aspose.words.fields](../)

