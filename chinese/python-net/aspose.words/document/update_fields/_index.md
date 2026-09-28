---
title: Document.update_fields method
linktitle: update_fields method
articleTitle: update_fields method
second_title: Aspose.Words for Python
description: "Document.update_fields method. Updates the values of fields in the whole document."
type: docs
weight: 800
url: /zh/python-net/aspose.words/document/update_fields/
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
# 为文档的首页插入目录。
# 配置目录以捕获级别 1 到 3 的标题段落。
# 此外，将其条目设置为超链接，使我们能够
# 在 Microsoft Word 中左键单击标题时跳转到标题位置。
builder.insert_table_of_contents('\\o "1-3" \\h \\z \\u')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# 通过添加带有标题样式的段落来填充目录。
# 每个级别在 1 到 3 之间的此类标题都会在目录中创建一个条目。
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
# 目录是需要更新以显示最新结果的字段类型。
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertToc.docx')
```

Shows to use the QUOTE field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 插入一个 QUOTE 字段，它将显示其 Text 属性的值。
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_QUOTE, update_field=True).as_field_quote()
field.text = '"Quoted text"'
self.assertEqual(' QUOTE  "\\"Quoted text\\""', field.get_field_code())
# 插入一个 QUOTE 字段，并在其中嵌套一个 DATE 字段。
# 每次使用 Microsoft Word 打开文档时，DATE 字段都会将其值更新为当前日期。
# 像这样将 DATE 字段嵌套在 QUOTE 字段中将冻结其值
# 为我们创建文档时的日期。
builder.write('\nDocument creation date: ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_QUOTE, update_field=True).as_field_quote()
builder.move_to(field.separator)
builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True)
self.assertEqual(' QUOTE \x13 DATE \x14' + str(date.today()) + '\x15', field.get_field_code())
# 更新所有字段以显示其正确的结果。
doc.update_fields()
self.assertEqual('"Quoted text"', doc.range.fields[0].result)
doc.save(file_name=ARTIFACTS_DIR + 'Field.QUOTE.docx')
```

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

* module [aspose.words](../../)
* class [Document](../)

