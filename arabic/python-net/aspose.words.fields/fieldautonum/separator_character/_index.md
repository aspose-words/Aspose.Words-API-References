---
title: FieldAutoNum.separator_character property
linktitle: separator_character property
articleTitle: separator_character property
second_title: Aspose.Words for Python
description: "FieldAutoNum.separator_character property. Gets or sets the separator character to be used."
type: docs
weight: 20
url: /ar/python-net/aspose.words.fields/fieldautonum/separator_character/
---

## FieldAutoNum.separator_character property

Gets or sets the separator character to be used.


```python
@property
def separator_character(self) -> str:
    ...

@separator_character.setter
def separator_character(self, value: str):
    ...

```

### Examples

Shows how to number paragraphs using autonum fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# يعرض كل حقل AUTONUM القيمة الحالية للعد المتسلسل لحقول AUTONUM،
# مما يسمح لنا بترقيم العناصر تلقائيًا مثل قائمة مرقمة.
# سيعرض هذا الحقل الرقم "1.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM, update_field=True).as_field_auto_num()
builder.writeln('\tParagraph 1.')
self.assertEqual(' AUTONUM ', field.get_field_code())
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM, update_field=True).as_field_auto_num()
builder.writeln('\tParagraph 2.')
# حرف الفاصل، الذي يظهر في نتيجة الحقل مباشرةً بعد الرقم، هو نقطة افتراضيًا.
# إذا تركنا هذه الخاصية فارغة (null)، سيعرض حقل AUTONUM الثاني "2." في المستند.
self.assertIsNone(field.separator_character)
# يمكننا ضبط هذه الخاصية لتطبيق الحرف الأول من سلسلتها كحرف الفاصل الجديد.
# في هذه الحالة، سيعرض حقل AUTONUM الخاص بنا الآن "2:".
field.separator_character = ':'
self.assertEqual(' AUTONUM  \\s :', field.get_field_code())
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTONUM.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNum](../)

