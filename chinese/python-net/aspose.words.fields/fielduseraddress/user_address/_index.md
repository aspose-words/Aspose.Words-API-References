---
title: FieldUserAddress.user_address property
linktitle: user_address property
articleTitle: user_address property
second_title: Aspose.Words for Python
description: "FieldUserAddress.user_address property. Gets or sets the current user's postal address."
type: docs
weight: 20
url: /zh/python-net/aspose.words.fields/fielduseraddress/user_address/
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
# 创建一个 UserInformation 对象，并将其设置为我们创建的任何字段的用户信息来源。
user_information = aw.fields.UserInformation()
user_information.address = '123 Main Street'
doc.field_options.current_user = user_information
# 创建一个 USERADDRESS 字段以显示当前用户的地址，
# 该名称取自我们上面创建的 UserInformation 对象。
builder = aw.DocumentBuilder(doc=doc)
field_user_address = builder.insert_field(field_type=aw.fields.FieldType.FIELD_USER_ADDRESS, update_field=True).as_field_user_address()
self.assertEqual(' USERADDRESS ', field_user_address.get_field_code())
self.assertEqual('123 Main Street', field_user_address.result)
# 我们可以设置此属性，使我们的字段覆盖当前存储在 UserInformation 对象中的值。
field_user_address.user_address = '456 North Road'
field_user_address.update()
self.assertEqual(' USERADDRESS  "456 North Road"', field_user_address.get_field_code())
self.assertEqual('456 North Road', field_user_address.result)
# 这不会影响 UserInformation 对象中的值。
self.assertEqual('123 Main Street', doc.field_options.current_user.address)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.USERADDRESS.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldUserAddress](../)

