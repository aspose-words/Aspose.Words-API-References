---
title: Document.update_fields method
linktitle: update_fields method
articleTitle: update_fields method
second_title: Aspose.Words for Python
description: "Document.update_fields method. Updates the values of fields in the whole document."
type: docs
weight: 800
url: /ru/python-net/aspose.words/document/update_fields/
---

## update_fields() {#default}

Updates the values of fields in the whole document.


```python
def update_fields(self):
    ...
```

### Remarks

When you open, modify and then save a document, Aspose.Words does not update fields automatically, it keeps them intact.
Therefore, you would usually want to call this method before saving if you have modified the document
programmatically and want to make sure the proper (calculated) field values appear in the saved document.

There is no need to update fields after executing a mail merge because mail merge is a kind of field update
and automatically updates all fields in the document.

This method does not update all field types. For the detailed list of supported field types, see the Programmers Guide.

This method does not update fields that are related to the page layout algorithms (e.g. PAGE, PAGES, PAGEREF).
The page layout-related fields are updated when you render a document or call [Document.update_page_layout()](../update_page_layout/#default).

Use the [Document.normalize_field_types()](../normalize_field_types/#default) method before fields updating if there were document changes that affected field types.

To update fields in a specific part of the document use [Range.update_fields()](../../range/update_fields/#default).




### Examples

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте оглавление на первую страницу документа.
# Настройте таблицу так, чтобы она захватывала абзацы с заголовками уровней от 1 до 3.
# Также установите, чтобы её элементы были гиперссылками, которые перенаправят нас
# к месту заголовка при щелчке левой кнопкой мыши в Microsoft Word.
builder.insert_table_of_contents('\\o "1-3" \\h \\z \\u')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Заполните оглавление, добавив абзацы со стилями заголовков.
# Каждый такой заголовок уровня от 1 до 3 создаст запись в таблице.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Heading 2')
builder.writeln('Heading 3')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 3.1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 3.1.1')
builder.writeln('Heading 3.1.2')
builder.writeln('Heading 3.1.3')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 3.1.3.1')
builder.writeln('Heading 3.1.3.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 3.2')
builder.writeln('Heading 3.3')
# Оглавление — это поле определённого типа, которое необходимо обновить, чтобы отобразить актуальный результат.
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertToc.docx')
```

Shows to use the QUOTE field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте поле QUOTE, которое будет отображать значение его свойства Text.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_QUOTE, update_field=True).as_field_quote()
field.text = '"Quoted text"'
self.assertEqual(' QUOTE  "\\"Quoted text\\""', field.get_field_code())
# Вставьте поле QUOTE и вложите в него поле DATE.
# Поля DATE обновляют своё значение до текущей даты каждый раз, когда мы открываем документ с помощью Microsoft Word.
# Вложение поля DATE внутрь поля QUOTE таким образом заморозит его значение
# на дату, когда мы создали документ.
builder.write('\nDocument creation date: ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_QUOTE, update_field=True).as_field_quote()
builder.move_to(field.separator)
builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True)
self.assertEqual(' QUOTE \x13 DATE \x14' + str(date.today()) + '\x15', field.get_field_code())
# Обновите все поля, чтобы отобразить их правильные результаты.
doc.update_fields()
self.assertEqual('"Quoted text"', doc.range.fields[0].result)
doc.save(file_name=ARTIFACTS_DIR + 'Field.QUOTE.docx')
```

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

* module [aspose.words](../../)
* class [Document](../)

