---
title: FieldUserName.user_name property
linktitle: user_name property
articleTitle: user_name property
second_title: Aspose.Words for Python
description: "FieldUserName.user_name property. Gest or sets the current user's name."
type: docs
weight: 20
url: /sv/python-net/aspose.words.fields/fieldusername/user_name/
---

## FieldUserName.user_name property

Gest or sets the current user's name.


```python
@property
def user_name(self) -> str:
    ...

@user_name.setter
def user_name(self, value: str):
    ...

```

### Examples

Shows how to use the USERNAME field.

```python
doc = aw.Document()
# Skapa ett UserInformation-objekt och ange det som källa för användarinformation för alla fält som vi skapar.
user_information = aw.fields.UserInformation()
user_information.name = 'John Doe'
doc.field_options.current_user = user_information
builder = aw.DocumentBuilder(doc=doc)
# Skapa ett USERNAME-fält för att visa den aktuella användarens namn,
# hämtat från UserInformation-objektet som vi skapade ovan.
field_user_name = builder.insert_field(field_type=aw.fields.FieldType.FIELD_USER_NAME, update_field=True).as_field_user_name()
self.assertEqual(user_information.name, field_user_name.result)
self.assertEqual(' USERNAME ', field_user_name.get_field_code())
self.assertEqual('John Doe', field_user_name.result)
# Vi kan ställa in den här egenskapen för att få vårt fält att åsidosätta värdet som för närvarande lagras i UserInformation-objektet.
field_user_name.user_name = 'Jane Doe'
field_user_name.update()
self.assertEqual(' USERNAME  "Jane Doe"', field_user_name.get_field_code())
self.assertEqual('Jane Doe', field_user_name.result)
# Detta påverkar inte värdet i UserInformation-objektet.
self.assertEqual('John Doe', doc.field_options.current_user.name)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.USERNAME.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldUserName](../)

