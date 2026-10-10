---
title: UserInformation.default_user property
linktitle: default_user property
articleTitle: default_user property
second_title: Aspose.Words for Python
description: "UserInformation.default_user property. Default user information."
type: docs
weight: 30
url: /zh/python-net/aspose.words.fields/userinformation/default_user/
---

## UserInformation.default_user property

Default user information.


```python
@property
def default_user(self) -> aspose.words.fields.UserInformation:
    ...

```

### Remarks

Use the [FieldOptions.current_user](../../fieldoptions/current_user/) property to specify user information for single document.



### Examples

Shows how to set user details, and display them using fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 创建一个 UserInformation 对象并将其设置为显示用户信息的字段的数据源。
user_information = aw.fields.UserInformation()
user_information.name = 'John Doe'
user_information.initials = 'J. D.'
user_information.address = '123 Main Street'
doc.field_options.current_user = user_information
# 插入 USERNAME、USERINITIALs 和 USERADDRESS 字段，这些字段显示
# 我们在上面创建的 UserInformation 对象的相应属性的值。
self.assertEqual(user_information.name, builder.insert_field(field_code=' USERNAME ').result)
self.assertEqual(user_information.initials, builder.insert_field(field_code=' USERINITIALS ').result)
self.assertEqual(user_information.address, builder.insert_field(field_code=' USERADDRESS ').result)
# 字段选项对象还具有一个静态默认用户，所有文档的字段都可以引用它。
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

