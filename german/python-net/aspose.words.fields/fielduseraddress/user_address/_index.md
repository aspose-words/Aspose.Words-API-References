---
title: FieldUserAddress.user_address property
linktitle: user_address property
articleTitle: user_address property
second_title: Aspose.Words for Python
description: "FieldUserAddress.user_address property. Gets or sets the current user's postal address."
type: docs
weight: 20
url: /de/python-net/aspose.words.fields/fielduseraddress/user_address/
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
# Erstellen Sie ein UserInformation-Objekt und setzen Sie es als Quelle der Benutzerinformationen für alle Felder, die wir erstellen.
user_information = aw.fields.UserInformation()
user_information.address = '123 Main Street'
doc.field_options.current_user = user_information
# Erstellen Sie ein USERADDRESS-Feld, um die aktuelle Benutzeradresse anzuzeigen,
# entnommen dem UserInformation-Objekt, das wir oben erstellt haben.
builder = aw.DocumentBuilder(doc=doc)
field_user_address = builder.insert_field(field_type=aw.fields.FieldType.FIELD_USER_ADDRESS, update_field=True).as_field_user_address()
self.assertEqual(' USERADDRESS ', field_user_address.get_field_code())
self.assertEqual('123 Main Street', field_user_address.result)
# Wir können diese Eigenschaft festlegen, damit unser Feld den derzeit im UserInformation-Objekt gespeicherten Wert überschreibt.
field_user_address.user_address = '456 North Road'
field_user_address.update()
self.assertEqual(' USERADDRESS  "456 North Road"', field_user_address.get_field_code())
self.assertEqual('456 North Road', field_user_address.result)
# Dies wirkt sich nicht auf den Wert im UserInformation-Objekt aus.
self.assertEqual('123 Main Street', doc.field_options.current_user.address)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.USERADDRESS.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldUserAddress](../)

