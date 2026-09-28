---
title: FieldEQ class
linktitle: FieldEQ class
articleTitle: FieldEQ class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldEQ class. Implements the EQ field"
type: docs
weight: 370
url: /ar/python-net/aspose.words.fields/fieldeq/
---

## FieldEQ class

Implements the EQ field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




**Inheritance:** [FieldEQ](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldEQ()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ as_office_math()](./as_office_math/#default) | Returns Office Math object corresponded to the EQ field. |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

### Examples

Shows how to use the EQ field to display a variety of mathematical equations.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# حقل EQ يعرض معادلة رياضية تتكون من عنصر واحد أو عدة عناصر.
# كل عنصر يأخذ الشكل التالي: [switch][options][arguments].
# قد يكون هناك مفتاح واحد، وعدة خيارات محتملة.
# المعطيات هي مجموعة من القيم المفصولة بفواصل ومغلقة بأقواس مستديرة.
# هنا نستخدم أداة بناء المستند لإدراج حقل EQ، مع مفتاح "\f"، والذي يتطابق مع "Fraction".
# سنمرّر القيم 1 و 4 كمعطيات، ولن نستخدم أي خيارات.
# هذا الحقل سيعرض كسرًا حيث 1 هو البسط و4 هو المقام.
field = ExField._insert_field_eq(builder, '\\f(1,4)')
self.assertEqual(' EQ \\f(1,4)', field.get_field_code())
# حقل EQ واحد قد يحتوي على عدة عناصر موضوعة بالتتابع.
# يمكننا أيضًا تضمين العناصر داخل بعضها البعض عن طريق وضع العناصر الداخلية
# داخل أقواس المعطيات للعناصر الخارجية.
# يمكننا العثور على القائمة الكاملة للمفاتيح، مع استخداماتها هنا:
# https:#blogs.msdn.microsoft.com/murrays/2018/01/23/microsoft-word-eq-field/
# فيما يلي تطبيقات لتسعة مفاتيح مختلفة لحقل EQ يمكننا استخدامها لإنشاء أنواع مختلفة من الكائنات.
# 1 -  مفتاح المصفوفة "\a", محاذاة إلى اليسار، عمودان، 3 نقاط من التباعد الأفقي والعمودي:
ExField._insert_field_eq(builder, '\\a \\al \\co2 \\vs3 \\hs3(4x,- 4y,-4x,+ y)')
# 2 -  مفتاح القوس "\b", حرف القوس "[", لإحاطة المحتوى بمجموعة من الأقواس المربعة:
# لاحظ أننا نقوم بتضمين مصفوفة داخل الأقواس، والتي ستظهر كأنها مصفوفة في الناتج.
ExField._insert_field_eq(builder, '\\b \\bc\\[ (\\a \\al \\co3 \\vs3 \\hs3(1,0,0,0,1,0,0,0,1))')
# 3 -  مفتاح الإزاحة "\d", إزاحة النص "B" 30 مسافة إلى يمين "A", عرض الفجوة كخط سفلي:
ExField._insert_field_eq(builder, 'A \\d \\fo30 \\li() B')
# 4 -  صيغة تتكون من عدة كسور:
ExField._insert_field_eq(builder, '\\f(d,dx)(u + v) = \\f(du,dx) + \\f(dv,dx)')
# 5 -  مفتاح التكامل "\i", مع رمز الجمع:
ExField._insert_field_eq(builder, '\\i \\su(n=1,5,n)')
# 6 -  مفتاح القائمة "\l":
ExField._insert_field_eq(builder, '\\l(1,1,2,3,n,8,13)')
# 7 -  مفتاح الجذر "\r", عرض الجذر التكعيبي للمتغير x:
ExField._insert_field_eq(builder, '\\r (3,x)')
# 8 -  مفتاح النص السفلي/العلوي "/s", أولاً كنص علوي ثم كنص سفلي:
ExField._insert_field_eq(builder, '\\s \\up8(Superscript) Text \\s \\do8(Subscript)')
# 9 -  مفتاح الصندوق "\x", مع خطوط في الأعلى، الأسفل، اليسار واليمين للمدخل:
ExField._insert_field_eq(builder, '\\x \\to \\bo \\le \\ri(5)')
# بعض التركيبات الأكثر تعقيدًا.
ExField._insert_field_eq(builder, '\\a \\ac \\vs1 \\co1(lim,n→∞) \\b (\\f(n,n2 + 12) + \\f(n,n2 + 22) + ... + \\f(n,n2 + n2))')
ExField._insert_field_eq(builder, '\\i (,,  \\b(\\f(x,x2 + 3x + 2))) \\s \\up10(2)')
ExField._insert_field_eq(builder, '\\i \\in( tan x, \\s \\up2(sec x), \\b(\\r(3) )\\s \\up4(t) \\s \\up7(2)  dt)')
doc.save(file_name=ARTIFACTS_DIR + 'Field.EQ.docx')
```

Shows how to use the EQ field to display a variety of mathematical equations (InsertFieldEQ).

```python
@staticmethod
def _insert_field_eq(builder, args):
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_EQUATION, update_field=True).as_field_eq()
    builder.move_to(field.separator)
    builder.write(args)
    builder.move_to(field.start.parent_node)
    builder.insert_paragraph()
    return field
```

Shows how to replace the EQ field with Office Math.

```python
doc = aw.Document(file_name=MY_DIR + 'Field sample - EQ.docx')
field_eq = list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_field_eq(), b), list(doc.range.fields))))[0]
office_math = field_eq.as_office_math()
field_eq.start.parent_node.insert_before(office_math, field_eq.start)
field_eq.remove()
doc.save(file_name=ARTIFACTS_DIR + 'Field.EQAsOfficeMath.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

