---
title: FieldUserAddress.user_address property
linktitle: user_address property
articleTitle: user_address property
second_title: Aspose.Words for Python
description: "FieldUserAddress.user_address property. Gets or sets the current user's postal address."
type: docs
weight: 20
url: /sv/python-net/aspose.words.fields/fielduseraddress/user_address/
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
# Skapa ett UserInformation-objekt och ange det som källa för användarinformation för alla fält som vi skapar.
user_information = aw.fields.UserInformation()
user_information.address = '123 Main Street'
doc.field_options.current_user = user_information
# Skapa ett USERADDRESS-fält för att visa den aktuella användarens adress,
# hämtat från UserInformation-objektet som vi skapade ovan.
builder = aw.DocumentBuilder(doc=doc)
field_user_address = builder.insert_field(field_type=aw.fields.FieldType.FIELD_USER_ADDRESS, update_field=True).as_field_user_address()
self.assertEqual(' USERADDRESS ', field_user_address.get_field_code())
self.assertEqual('123 Main Street', field_user_address.result)
# Vi kan ställa in den här egenskapen för att få vårt fält att åsidosätta värdet som för närvarande lagras i UserInformation-objektet.
field_user_address.user_address = '456 North Road'
field_user_address.update()
self.assertEqual(' USERADDRESS  "456 North Road"', field_user_address.get_field_code())
self.assertEqual('456 North Road', field_user_address.result)
# Detta påverkar inte värdet i UserInformation-objektet.
self.assertEqual('123 Main Street', doc.field_options.current_user.address)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.USERADDRESS.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldUserAddress](../)

