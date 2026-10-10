---
title: UserInformation.address property
linktitle: address property
articleTitle: address property
second_title: Aspose.Words for Python
description: "UserInformation.address property. Gets or sets the user's postal address."
type: docs
weight: 20
url: /it/python-net/aspose.words.fields/userinformation/address/
---

## UserInformation.address property

Gets or sets the user's postal address.


```python
@property
def address(self) -> str:
    ...

@address.setter
def address(self, value: str):
    ...

```

### Examples

Shows how to set user details, and display them using fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Crea un oggetto UserInformation e impostalo come origine dati per i campi che visualizzano le informazioni dell'utente.
user_information = aw.fields.UserInformation()
user_information.name = 'John Doe'
user_information.initials = 'J. D.'
user_information.address = '123 Main Street'
doc.field_options.current_user = user_information
# Inserisci i campi USERNAME, USERINITIALS e USERADDRESS, che visualizzano i valori di
# le rispettive proprietà dell'oggetto UserInformation che abbiamo creato sopra.
self.assertEqual(user_information.name, builder.insert_field(field_code=' USERNAME ').result)
self.assertEqual(user_information.initials, builder.insert_field(field_code=' USERINITIALS ').result)
self.assertEqual(user_information.address, builder.insert_field(field_code=' USERADDRESS ').result)
# L'oggetto opzioni campo ha anche un utente predefinito statico a cui i campi di tutti i documenti possono fare riferimento.
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

