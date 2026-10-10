---
title: Document.update_fields method
linktitle: update_fields method
articleTitle: update_fields method
second_title: Aspose.Words for Python
description: "Document.update_fields method. Updates the values of fields in the whole document."
type: docs
weight: 800
url: /ar/python-net/aspose.words/document/update_fields/
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
# أدرج جدول محتويات للصفحة الأولى من المستند.
# قم بتكوين الجدول لالتقاط الفقرات ذات العناوين من المستوى 1 إلى 3.
# أيضًا، اضبط عناصره لتكون روابط تشعبية ستأخذنا
# إلى موقع العنوان عند النقر بزر الفأرة الأيسر في Microsoft Word.
builder.insert_table_of_contents('\\o "1-3" \\h \\z \\u')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# املأ جدول المحتويات بإضافة فقرات باستخدام أنماط العناوين.
# كل عنوان من هذا النوع بمستوى بين 1 و 3 سيُنشئ مدخلاً في الجدول.
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
# جدول المحتويات هو حقل من نوع يحتاج إلى تحديث لإظهار نتيجة محدثة.
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertToc.docx')
```

Shows to use the QUOTE field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أدرج حقل QUOTE، الذي سيعرض قيمة خاصية Text الخاصة به.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_QUOTE, update_field=True).as_field_quote()
field.text = '"Quoted text"'
self.assertEqual(' QUOTE  "\\"Quoted text\\""', field.get_field_code())
# أدرج حقل QUOTE وضع داخله حقل DATE.
# حقول DATE تُحدّث قيمتها إلى التاريخ الحالي في كل مرة نفتح فيها المستند باستخدام Microsoft Word.
# وضع حقل DATE داخل حقل QUOTE بهذه الطريقة سيجمد قيمته
# إلى التاريخ الذي أنشأنا فيه المستند.
builder.write('\nDocument creation date: ')
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_QUOTE, update_field=True).as_field_quote()
builder.move_to(field.separator)
builder.insert_field(field_type=aw.fields.FieldType.FIELD_DATE, update_field=True)
self.assertEqual(' QUOTE \x13 DATE \x14' + str(date.today()) + '\x15', field.get_field_code())
# حدّث جميع الحقول لعرض نتائجها الصحيحة.
doc.update_fields()
self.assertEqual('"Quoted text"', doc.range.fields[0].result)
doc.save(file_name=ARTIFACTS_DIR + 'Field.QUOTE.docx')
```

Shows how to set user details, and display them using fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# إنشاء كائن UserInformation وتعيينه كمصدر بيانات للحقول التي تعرض معلومات المستخدم.
user_information = aw.fields.UserInformation()
user_information.name = 'John Doe'
user_information.initials = 'J. D.'
user_information.address = '123 Main Street'
doc.field_options.current_user = user_information
# إدراج حقول USERNAME و USERINITIALS و USERADDRESS، التي تعرض قيم
# الخصائص المقابلة لكائن UserInformation الذي أنشأناه أعلاه.
self.assertEqual(user_information.name, builder.insert_field(field_code=' USERNAME ').result)
self.assertEqual(user_information.initials, builder.insert_field(field_code=' USERINITIALS ').result)
self.assertEqual(user_information.address, builder.insert_field(field_code=' USERADDRESS ').result)
# كائن خيارات الحقل يحتوي أيضًا على مستخدم افتراضي ثابت يمكن للحقول في جميع المستندات الإشارة إليه.
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

