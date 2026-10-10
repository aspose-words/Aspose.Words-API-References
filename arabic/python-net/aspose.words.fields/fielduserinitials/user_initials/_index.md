---
title: FieldUserInitials.user_initials property
linktitle: user_initials property
articleTitle: user_initials property
second_title: Aspose.Words for Python
description: "FieldUserInitials.user_initials property. Gets or sets the current user's initials."
type: docs
weight: 20
url: /ar/python-net/aspose.words.fields/fielduserinitials/user_initials/
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
# أنشئ كائن UserInformation واضبطه كمصدر لمعلومات المستخدم لأي حقول نقوم بإنشائها.
user_information = aw.fields.UserInformation()
user_information.initials = 'J. D.'
doc.field_options.current_user = user_information
# أنشئ حقل USERINITIALS لعرض الأحرف الأولى للمستخدم الحالي،
# مستمد من كائن UserInformation الذي أنشأناه أعلاه.
builder = aw.DocumentBuilder(doc=doc)
field_user_initials = builder.insert_field(field_type=aw.fields.FieldType.FIELD_USER_INITIALS, update_field=True).as_field_user_initials()
self.assertEqual(user_information.initials, field_user_initials.result)
self.assertEqual(' USERINITIALS ', field_user_initials.get_field_code())
self.assertEqual('J. D.', field_user_initials.result)
# يمكننا ضبط هذه الخاصية لجعل الحقل يتجاوز القيمة المخزنة حالياً في كائن UserInformation.
field_user_initials.user_initials = 'J. C.'
field_user_initials.update()
self.assertEqual(' USERINITIALS  "J. C."', field_user_initials.get_field_code())
self.assertEqual('J. C.', field_user_initials.result)
# هذا لا يؤثر على القيمة في كائن UserInformation.
self.assertEqual('J. D.', doc.field_options.current_user.initials)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.USERINITIALS.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldUserInitials](../)

