---
title: FieldAutoNumLgl.separator_character property
linktitle: separator_character property
articleTitle: separator_character property
second_title: Aspose.Words for Python
description: "FieldAutoNumLgl.separator_character property. Gets or sets the separator character to be used."
type: docs
weight: 30
url: /ar/python-net/aspose.words.fields/fieldautonumlgl/separator_character/
---

## FieldAutoNumLgl.separator_character property

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

Shows how to organize a document using AUTONUMLGL fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
filler_text = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ' + '\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. '
# حقول AUTONUMLGL تعرض رقمًا يزداد في كل حقل AUTONUMLGL ضمن مستوى العنوان الحالي.
# تحافظ هذه الحقول على عدّ منفصل لكل مستوى عنوان،
# ويعرض كل حقل أيضًا عدد حقول AUTONUMLGL لجميع مستويات العناوين أدنى مستواه.
# تغيير العدد لأي مستوى عنوان يعيد ضبط العد لجميع المستويات فوق ذلك المستوى إلى 1.
# هذا يسمح لنا بتنظيم مستندنا على شكل قائمة مخطط.
# هذا هو الحقل AUTONUMLGL الأول على مستوى عنوان 1، يعرض "1." في المستند.
ExField._insert_numbered_clause(builder, '\tHeading 1', filler_text, aw.StyleIdentifier.HEADING1)
# هذا هو الحقل AUTONUMLGL الثاني على مستوى عنوان 1، لذا سيعرض "2.".
ExField._insert_numbered_clause(builder, '\tHeading 2', filler_text, aw.StyleIdentifier.HEADING1)
# هذا هو الحقل AUTONUMLGL الأول على مستوى عنوان 2،
# وعدد AUTONUMLGL للمستوى الذي أسفله هو "2"، لذا سيعرض "2.1.".
ExField._insert_numbered_clause(builder, '\tHeading 3', filler_text, aw.StyleIdentifier.HEADING2)
# هذا هو الحقل AUTONUMLGL الأول على مستوى عنوان 3.
# يعمل بنفس طريقة الحقل أعلاه، سيعرض "2.1.1.".
ExField._insert_numbered_clause(builder, '\tHeading 4', filler_text, aw.StyleIdentifier.HEADING3)
# هذا الحقل على مستوى عنوان 2، وعدده AUTONUMLGL المقابل هو 2، لذا سيعرض الحقل "2.2.".
ExField._insert_numbered_clause(builder, '\tHeading 5', filler_text, aw.StyleIdentifier.HEADING2)
# زيادة عدد AUTONUMLGL لمستوى عنوان أدنى من هذا
# قد أعاد ضبط العدد لهذا المستوى بحيث سيعرض هذا الحقل "2.2.1.".
ExField._insert_numbered_clause(builder, '\tHeading 6', filler_text, aw.StyleIdentifier.HEADING3)
for field in list(filter(lambda f: f.type == aw.fields.FieldType.FIELD_AUTO_NUM_LEGAL, list(doc.range.fields))):
    field = field.as_field_auto_num_lgl()
    # حرف الفاصل، الذي يظهر في نتيجة الحقل مباشرةً بعد الرقم،
    # هو نقطة (.) بشكل افتراضي. إذا تركنا هذه الخاصية فارغة،
    # سيعرض حقل AUTONUMLGL الأخير "2.2.1." في المستند.
    self.assertIsNone(field.separator_character)
    # تعيين حرف فاصل مخصص وإزالة النقطة اللاحقة
    # سيغير مظهر ذلك الحقل من "2.2.1." إلى "2:2:1".
    # سنطبق ذلك على جميع الحقول التي أنشأناها.
    field.separator_character = ':'
    field.remove_trailing_period = True
    self.assertEqual(' AUTONUMLGL  \\s : \\e', field.get_field_code())
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTONUMLGL.docx')
```

Shows how to organize a document using AUTONUMLGL fields (InsertNumberedClause).

```python
@staticmethod
def _insert_numbered_clause(builder, heading, contents, heading_style):
    builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM_LEGAL, update_field=True)
    builder.current_paragraph.paragraph_format.style_identifier = heading_style
    builder.writeln(heading)
    # هذا النص سيخص الحقل القانوني التلقائي أعلاه.
    # سيتقلص عندما نضغط على السهم بجوار الحقل AUTONUMLGL المقابل في Microsoft Word.
    builder.current_paragraph.paragraph_format.style_identifier = aw.StyleIdentifier.BODY_TEXT
    builder.writeln(contents)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNumLgl](../)

