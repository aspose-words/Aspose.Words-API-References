---
title: FieldUserName.user_name property
linktitle: user_name property
articleTitle: user_name property
second_title: Aspose.Words for Python
description: "FieldUserName.user_name property. Gest or sets the current user's name."
type: docs
weight: 20
url: /ar/python-net/aspose.words.fields/fieldusername/user_name/
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
# أنشئ كائن UserInformation واضبطه كمصدر لمعلومات المستخدم لأي حقول نقوم بإنشائها.
user_information = aw.fields.UserInformation()
user_information.name = 'John Doe'
doc.field_options.current_user = user_information
builder = aw.DocumentBuilder(doc=doc)
# أنشئ حقل USERNAME لعرض اسم المستخدم الحالي،
# مستمد من كائن UserInformation الذي أنشأناه أعلاه.
field_user_name = builder.insert_field(field_type=aw.fields.FieldType.FIELD_USER_NAME, update_field=True).as_field_user_name()
self.assertEqual(user_information.name, field_user_name.result)
self.assertEqual(' USERNAME ', field_user_name.get_field_code())
self.assertEqual('John Doe', field_user_name.result)
# يمكننا ضبط هذه الخاصية لجعل الحقل يتجاوز القيمة المخزنة حالياً في كائن UserInformation.
field_user_name.user_name = 'Jane Doe'
field_user_name.update()
self.assertEqual(' USERNAME  "Jane Doe"', field_user_name.get_field_code())
self.assertEqual('Jane Doe', field_user_name.result)
# هذا لا يؤثر على القيمة في كائن UserInformation.
self.assertEqual('John Doe', doc.field_options.current_user.name)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.USERNAME.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldUserName](../)

