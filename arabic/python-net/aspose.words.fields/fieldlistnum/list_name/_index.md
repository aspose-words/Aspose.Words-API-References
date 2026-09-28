---
title: FieldListNum.list_name property
linktitle: list_name property
articleTitle: list_name property
second_title: Aspose.Words for Python
description: "FieldListNum.list_name property. Gets or sets the name of the abstract numbering definition used for the numbering."
type: docs
weight: 40
url: /ar/python-net/aspose.words.fields/fieldlistnum/list_name/
---

## FieldListNum.list_name property

Gets or sets the name of the abstract numbering definition used for the numbering.


```python
@property
def list_name(self) -> str:
    ...

@list_name.setter
def list_name(self, value: str):
    ...

```

### Examples

Shows how to number paragraphs with LISTNUM fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# حقول LISTNUM تعرض رقمًا يزداد في كل حقل LISTNUM.
# تحتوي هذه الحقول أيضًا على مجموعة متنوعة من الخيارات التي تسمح لنا باستخدامها لمحاكاة القوائم المرقمة.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
# تبدأ القوائم العد من 1 افتراضيًا، لكن يمكننا ضبط هذا الرقم إلى قيمة مختلفة، مثل 0.
# سيعرض هذا الحقل \"0)\".
field.starting_number = '0'
builder.writeln('Paragraph 1')
self.assertEqual(' LISTNUM  \\s 0', field.get_field_code())
# حقول LISTNUM تحافظ على عدّ منفصل لكل مستوى قائمة.
# إدراج حقل LISTNUM في نفس الفقرة مع حقل LISTNUM آخر
# يزيد مستوى القائمة بدلاً من العد.
# الحقل التالي سيستمر في العد الذي بدأناه أعلاه ويعرض قيمة \"1\" في مستوى القائمة 1.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# هذا الحقل سيبدأ عدًا في مستوى القائمة 2. سيعرض قيمة \"1\".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# هذا الحقل سيبدأ عدًا في مستوى القائمة 3. سيعرض قيمة \"1\".
# مستويات القوائم المختلفة لها تنسيق مختلف،
# لذلك هذه الحقول مجتمعة ستعرض قيمة "1)a)i)".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
builder.writeln('Paragraph 2')
# حقل LISTNUM التالي الذي نقوم بإدراجه سيستمر في العد عند مستوى القائمة
# الذي كان عليه حقل LISTNUM السابق.
# يمكننا استخدام الخاصية "ListLevel" للانتقال إلى مستوى قائمة مختلف.
# إذا ظل هذا الحقل LISTNUM على مستوى القائمة 3، فسيعرض "ii)",
# ولكن، بما أننا نقلناه إلى مستوى القائمة 2، فإنه يواصل العد عند ذلك المستوى ويعرض "b)".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_level = '2'
builder.writeln('Paragraph 3')
self.assertEqual(' LISTNUM  \\l 2', field.get_field_code())
# يمكننا ضبط الخاصية ListName لجعل الحقل يحاكي نوع حقل AUTONUM مختلف.
# "NumberDefault" يحاكي AUTONUM، "OutlineDefault" يحاكي AUTONUMOUT،
# و "LegalDefault" يحاكي حقول AUTONUMLGL.
# اسم القائمة "OutlineDefault" مع الرقم 1 كبداية سيؤدي إلى عرض "I.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.starting_number = '1'
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 4')
self.assertTrue(field.has_list_name)
self.assertEqual(' LISTNUM  OutlineDefault \\s 1', field.get_field_code())
# خاصية ListName لا تنتقل من الحقل السابق، لذا سنحتاج إلى ضبطها لكل حقل جديد.
# هذا الحقل يواصل العد باستخدام اسم القائمة المختلف ويعرض "II.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 5')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.LISTNUM.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldListNum](../)

