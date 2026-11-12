---
title: FieldOptions.current_user property
linktitle: current_user property
articleTitle: current_user property
second_title: Aspose.Words for Python
description: "FieldOptions.current_user property. Gets or sets the current user information."
type: docs
weight: 50
url: /ru/python-net/aspose.words.fields/fieldoptions/current_user/
---

## FieldOptions.current_user property

Gets or sets the current user information.


```python
@property
def current_user(self) -> aspose.words.fields.UserInformation:
    ...

@current_user.setter
def current_user(self, value: aspose.words.fields.UserInformation):
    ...

```

### Examples

Shows how to set user details, and display them using fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Создайте объект UserInformation и установите его в качестве источника данных для полей, отображающих информацию о пользователе.
user_information = aw.fields.UserInformation()
user_information.name = 'John Doe'
user_information.initials = 'J. D.'
user_information.address = '123 Main Street'
doc.field_options.current_user = user_information
# Вставьте поля USERNAME, USERINITIALS и USERADDRESS, которые отображают значения
# соответствующих свойств объекта UserInformation, который мы создали выше.
self.assertEqual(user_information.name, builder.insert_field(field_code=' USERNAME ').result)
self.assertEqual(user_information.initials, builder.insert_field(field_code=' USERINITIALS ').result)
self.assertEqual(user_information.address, builder.insert_field(field_code=' USERADDRESS ').result)
# Объект параметров полей также имеет статического пользователя по умолчанию, к которому могут обращаться поля из всех документов.
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
* class [FieldOptions](../)

