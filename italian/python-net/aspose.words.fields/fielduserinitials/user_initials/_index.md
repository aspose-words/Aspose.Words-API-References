---
title: FieldUserInitials.user_initials property
linktitle: user_initials property
articleTitle: user_initials property
second_title: Aspose.Words for Python
description: "FieldUserInitials.user_initials property. Gets or sets the current user's initials."
type: docs
weight: 20
url: /it/python-net/aspose.words.fields/fielduserinitials/user_initials/
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
# Crea un oggetto UserInformation e impostalo come fonte delle informazioni utente per tutti i campi che creiamo.
user_information = aw.fields.UserInformation()
user_information.initials = 'J. D.'
doc.field_options.current_user = user_information
# Crea un campo USERINITIALS per visualizzare le iniziali dell'utente corrente,
# preso dall'oggetto UserInformation che abbiamo creato sopra.
builder = aw.DocumentBuilder(doc=doc)
field_user_initials = builder.insert_field(field_type=aw.fields.FieldType.FIELD_USER_INITIALS, update_field=True).as_field_user_initials()
self.assertEqual(user_information.initials, field_user_initials.result)
self.assertEqual(' USERINITIALS ', field_user_initials.get_field_code())
self.assertEqual('J. D.', field_user_initials.result)
# Possiamo impostare questa proprietà per far sì che il nostro campo sovrascriva il valore attualmente memorizzato nell'oggetto UserInformation.
field_user_initials.user_initials = 'J. C.'
field_user_initials.update()
self.assertEqual(' USERINITIALS  "J. C."', field_user_initials.get_field_code())
self.assertEqual('J. C.', field_user_initials.result)
# Questo non influisce sul valore nell'oggetto UserInformation.
self.assertEqual('J. D.', doc.field_options.current_user.initials)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.USERINITIALS.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldUserInitials](../)

