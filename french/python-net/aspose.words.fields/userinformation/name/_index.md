---
title: UserInformation.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Python
description: "UserInformation.name property. Gets or sets the user's name."
type: docs
weight: 50
url: /fr/python-net/aspose.words.fields/userinformation/name/
---

## UserInformation.name property

Gets or sets the user's name.


```python
@property
def name(self) -> str:
    ...

@name.setter
def name(self, value: str):
    ...

```

### Examples

Shows how to set user details, and display them using fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Créez un objet UserInformation et définissez-le comme source de données pour les champs qui affichent les informations utilisateur.
user_information = aw.fields.UserInformation()
user_information.name = 'John Doe'
user_information.initials = 'J. D.'
user_information.address = '123 Main Street'
doc.field_options.current_user = user_information
# Insérez les champs USERNAME, USERINITIALS et USERADDRESS, qui affichent les valeurs de
# les propriétés respectives de l'objet UserInformation que nous avons créé ci‑dessus.
self.assertEqual(user_information.name, builder.insert_field(field_code=' USERNAME ').result)
self.assertEqual(user_information.initials, builder.insert_field(field_code=' USERINITIALS ').result)
self.assertEqual(user_information.address, builder.insert_field(field_code=' USERADDRESS ').result)
# L'objet d'options de champ possède également un utilisateur par défaut statique auquel les champs de tous les documents peuvent se référer.
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

