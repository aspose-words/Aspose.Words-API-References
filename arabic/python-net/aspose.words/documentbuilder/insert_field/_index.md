---
title: DocumentBuilder.insert_field method
linktitle: insert_field method
articleTitle: insert_field method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_field method"
type: docs
weight: 330
url: /ar/python-net/aspose.words/documentbuilder/insert_field/
---

## insert_field(field_type, update_field) {#fieldtype_bool}

Inserts a Word field into a document and optionally updates the field result.


```python
def insert_field(self, field_type: aspose.words.fields.FieldType, update_field: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field_type | [FieldType](../../../aspose.words.fields/fieldtype/) | The type of the field to append. |
| update_field | bool | Specifies whether to update the field immediately. |

### Remarks

This method inserts a field into a document.
Aspose.Words can update fields of most types, but not all. For more details see the
[DocumentBuilder.insert_field()](./#str_str) overload.




### Returns

A [Field](../../../aspose.words.fields/field/) object that represents the inserted field.


## insert_field(field_code) {#str}

Inserts a Word field into a document and updates the field result.


```python
def insert_field(self, field_code: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field_code | str | The field code to insert (without curly braces). |

### Remarks

This method inserts a field into a document and updates the field result immediately.
Aspose.Words can update fields of most types, but not all. For more details see the
[DocumentBuilder.insert_field()](./#str_str) overload.




### Returns

A [Field](../../../aspose.words.fields/field/) object that represents the inserted field.


## insert_field(field_code, field_value) {#str_str}

Inserts a Word field into a document without updating the field result.


```python
def insert_field(self, field_code: str, field_value: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| field_code | str | The field code to insert (without curly braces). |
| field_value | str | The field value to insert. Pass ``None`` for fields that do not have a value. |

### Remarks

Fields in Microsoft Word documents consist of a field code and a field result.
The field code is like a formula and the field result is like the value that
the formula produces. The field code may also contain field switches
that are like additional instructions to perform a specific action.

You can switch between displaying field codes and results in your document in
Microsoft Word using the keyboard shortcut Alt+F9. Field codes appear between curly braces ( { } ).

To create a field, you need to specify a field type, field code and a "placeholder" field value.
If you are not sure about a particular field code syntax, create the field in Microsoft Word first
and switch to see its field code.

Aspose.Words can calculate field results for most of the field types, but this method
does not update the field result automatically. Because the field result is not calculated automatically,
you are expected to pass some string value (or even an empty string) that will be inserted into the field result.
This value will remain in the field result as a placeholder until the field is updated.
To update the field result you can call [Field.update()](../../../aspose.words.fields/field/update/#default) on the field object returned
to you or [Document.update_fields()](../../document/update_fields/#default) to update fields in the whole document.




### Returns

A [Field](../../../aspose.words.fields/field/) object that represents the inserted field.


## Examples

Shows how to insert a field into a document using FieldType.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أدرج حقلين مع تمرير علامة تحدد ما إذا كان سيتم تحديثهما أثناء إدراج الباني لهما.
# في بعض الحالات، قد يكون تحديث الحقول مكلفًا حسابيًا، وقد يكون من الجيد تأجيل التحديث.
doc.built_in_document_properties.author = 'John Doe'
builder.write('This document was written by ')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=update_inserted_fields_immediately)
builder.insert_paragraph()
builder.write('\nThis is page ')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_PAGE, update_field=update_inserted_fields_immediately)
self.assertEqual(' AUTHOR ', doc.range.fields[0].get_field_code())
self.assertEqual(' PAGE ', doc.range.fields[1].get_field_code())
if update_inserted_fields_immediately:
    self.assertEqual('John Doe', doc.range.fields[0].result)
    self.assertEqual('1', doc.range.fields[1].result)
else:
    self.assertEqual('', doc.range.fields[0].result)
    self.assertEqual('', doc.range.fields[1].result)
    # سنحتاج إلى تحديث هذه الحقول يدويًا باستخدام طرق التحديث.
    doc.range.fields[0].update()
    self.assertEqual('John Doe', doc.range.fields[0].result)
    doc.update_fields()
    self.assertEqual('1', doc.range.fields[1].result)
```

Shows how to insert fields, and move the document builder's cursor to them.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_field(field_code='MERGEFIELD MyMergeField1 \\* MERGEFORMAT')
builder.insert_field(field_code='MERGEFIELD MyMergeField2 \\* MERGEFORMAT')
# انقل المؤشر إلى أول MERGEFIELD.
builder.move_to_merge_field(field_name='MyMergeField1', is_after=True, is_delete_field=False)
# لاحظ أن المؤشر يُوضع مباشرة بعد أول MERGEFIELD، وقبل الثاني.
self.assertEqual(doc.range.fields[1].start, builder.current_node)
self.assertEqual(doc.range.fields[0].end, builder.current_node.previous_sibling)
# إذا رغبنا في تعديل شفرة الحقل أو محتوياته باستخدام builder،
# سيحتاج مؤشره إلى أن يكون داخل حقل.
# لوضعه داخل حقل، سنحتاج إلى استدعاء طريقة MoveTo الخاصة بـ document builder
# وتمرير عقدة بداية الحقل أو الفاصل كمعامل.
builder.write(' Text between our merge fields. ')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.MergeFields.docx')
```

Shows how to insert a field into a document using a field code.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
field = builder.insert_field('DATE \\@ "dddd, MMMM dd, yyyy"')
self.assertEqual(aw.fields.FieldType.FIELD_DATE, field.type)
self.assertEqual('DATE \\@ "dddd, MMMM dd, yyyy"', field.get_field_code())
# هذا التحميل الزائد للطريقة "insert_field" يقوم تلقائيًا بتحديث الحقول المُدرجة.
self.assertAlmostEqual(datetime.datetime.strptime(field.result, '%A, %B %d, %Y'), datetime.datetime.now(), delta=timedelta(1))
```

Shows how to set up page numbering in a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Section 1, page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 1, page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 1, page 3.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln('Section 2, page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 2, page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 2, page 3.')
# انقل مُنشئ المستند إلى الترويسة الأساسية للقسم الأول،
# التي سيعرضها كل صفحة في ذلك القسم.
builder.move_to_section(0)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
# أدرج حقل PAGE، الذي سيعرض رقم الصفحة الحالية.
builder.write('Page ')
builder.insert_field(field_code='PAGE', field_value='')
# قم بتهيئة القسم بحيث يبدأ عدد الصفحات الذي تعرضه حقول PAGE من 5.
# أيضًا، قم بتهيئة جميع حقول PAGE لعرض أرقام الصفحات باستخدام أرقام رومانية كبيرة.
page_setup = doc.sections[0].page_setup
page_setup.restart_page_numbering = True
page_setup.page_starting_number = 5
page_setup.page_number_style = aw.NumberStyle.UPPERCASE_ROMAN
# أنشئ ترويسة أساسية أخرى للقسم الثاني، مع حقل PAGE آخر.
builder.move_to_section(1)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.write(' - ')
builder.insert_field(field_code='PAGE', field_value='')
builder.write(' - ')
# قم بتهيئة القسم بحيث يبدأ عدد الصفحات الذي تعرضه حقول PAGE من 10.
# أيضًا، قم بتهيئة جميع حقول PAGE لعرض أرقام الصفحات باستخدام الأرقام العربية.
page_setup = doc.sections[1].page_setup
page_setup.page_starting_number = 10
page_setup.restart_page_numbering = True
page_setup.page_number_style = aw.NumberStyle.ARABIC
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PageNumbering.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)
* class [Field](../../../aspose.words.fields/field/)

