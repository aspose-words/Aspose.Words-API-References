---
title: FieldUserInitials.user_initials property
linktitle: user_initials property
articleTitle: user_initials property
second_title: Aspose.Words for Python
description: "FieldUserInitials.user_initials property. Gets or sets the current user's initials."
type: docs
weight: 20
url: /zh/python-net/aspose.words.fields/fielduserinitials/user_initials/
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
# 创建一个 UserInformation 对象，并将其设置为我们创建的任何字段的用户信息来源。
user_information = aw.fields.UserInformation()
user_information.initials = 'J. D.'
doc.field_options.current_user = user_information
# 创建一个 USERINITIALS 字段以显示当前用户的首字母缩写，
# 该名称取自我们上面创建的 UserInformation 对象。
builder = aw.DocumentBuilder(doc=doc)
field_user_initials = builder.insert_field(field_type=aw.fields.FieldType.FIELD_USER_INITIALS, update_field=True).as_field_user_initials()
self.assertEqual(user_information.initials, field_user_initials.result)
self.assertEqual(' USERINITIALS ', field_user_initials.get_field_code())
self.assertEqual('J. D.', field_user_initials.result)
# 我们可以设置此属性，使我们的字段覆盖当前存储在 UserInformation 对象中的值。
field_user_initials.user_initials = 'J. C.'
field_user_initials.update()
self.assertEqual(' USERINITIALS  "J. C."', field_user_initials.get_field_code())
self.assertEqual('J. C.', field_user_initials.result)
# 这不会影响 UserInformation 对象中的值。
self.assertEqual('J. D.', doc.field_options.current_user.initials)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.USERINITIALS.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldUserInitials](../)

