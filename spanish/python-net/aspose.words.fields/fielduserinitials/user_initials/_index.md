---
title: FieldUserInitials.user_initials property
linktitle: user_initials property
articleTitle: user_initials property
second_title: Aspose.Words for Python
description: "FieldUserInitials.user_initials property. Gets or sets the current user's initials."
type: docs
weight: 20
url: /es/python-net/aspose.words.fields/fielduserinitials/user_initials/
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
# Crea un objeto UserInformation y establécelo como la fuente de información del usuario para cualquier campo que creemos.
user_information = aw.fields.UserInformation()
user_information.initials = 'J. D.'
doc.field_options.current_user = user_information
# Cree un campo USERINITIALS para mostrar las iniciales del usuario actual,
# tomado del objeto UserInformation que creamos arriba.
builder = aw.DocumentBuilder(doc=doc)
field_user_initials = builder.insert_field(field_type=aw.fields.FieldType.FIELD_USER_INITIALS, update_field=True).as_field_user_initials()
self.assertEqual(user_information.initials, field_user_initials.result)
self.assertEqual(' USERINITIALS ', field_user_initials.get_field_code())
self.assertEqual('J. D.', field_user_initials.result)
# Podemos establecer esta propiedad para que nuestro campo sobrescriba el valor almacenado actualmente en el objeto UserInformation.
field_user_initials.user_initials = 'J. C.'
field_user_initials.update()
self.assertEqual(' USERINITIALS  "J. C."', field_user_initials.get_field_code())
self.assertEqual('J. C.', field_user_initials.result)
# Esto no afecta el valor en el objeto UserInformation.
self.assertEqual('J. D.', doc.field_options.current_user.initials)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.USERINITIALS.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldUserInitials](../)

