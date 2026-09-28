---
title: FieldShape.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldShape.text property. Gets or sets the text to retrieve."
type: docs
weight: 20
url: /ar/python-net/aspose.words.fields/fieldshape/text/
---

## FieldShape.text property

Gets or sets the text to retrieve.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Examples

Shows how to create right-to-left language-compatible lists with BIDIOUTLINE fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# حقل BIDIOUTLINE يرقم الفقرات مثل حقول AUTONUM/LISTNUM،
# ولكنه يظهر فقط عندما يتم تمكين لغة تحرير من اليمين إلى اليسار، مثل العبرية أو العربية.
# الحقل التالي سيعرض ".1"، وهو المكافئ RTL للرقم القائم "1.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True).as_field_bidi_outline()
builder.writeln('שלום')
self.assertEqual(' BIDIOUTLINE ', field.get_field_code())
# أضف حقلين آخرين من نوع BIDIOUTLINE، سيعرضان ".2" و ".3".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
# ضبط محاذاة النص الأفقية لكل فقرة في المستند إلى RTL.
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    para.paragraph_format.bidi = True
# إذا فعلنا لغة تحرير من اليمين إلى اليسار في Microsoft Word، ستعرض حقولنا أرقامًا.
# وإلا، ستعرض "###".
doc.save(file_name=ARTIFACTS_DIR + 'Field.BIDIOUTLINE.docx')
```

Shows how some older Microsoft Word fields such as SHAPE and EMBED are handled during loading.

```python
# افتح مستندًا تم إنشاؤه في Microsoft Word 2003.
doc = aw.Document(file_name=MY_DIR + 'Legacy fields.doc')
# إذا فتحنا مستند Word وضغطنا Alt+F9، سنرى حقل SHAPE وحقل EMBED.
# حقل SHAPE هو المرساة/اللوحة لكائن AutoShape مع تمكين نمط الالتفاف "In line with text".
# حقل EMBED له نفس الوظيفة، لكنه لكائن مضمّن،
# مثل جدول بيانات من مستند Excel خارجي.
# مع ذلك، هذه الحقول لن تظهر في مجموعة حقول المستند.
self.assertEqual(0, doc.range.fields.count)
# هذه الحقول مدعومة فقط في الإصدارات القديمة من Microsoft Word.
# عملية تحميل المستند ستحول هذه الحقول إلى كائنات Shape،
# والتي يمكننا الوصول إليها في مجموعة عقد المستند.
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)
self.assertEqual(3, shapes.count)
# العقدة الأولى من نوع Shape تتطابق مع حقل SHAPE في المستند المدخل،
# وهي اللوحة المضمنة لكائن AutoShape.
shape = shapes[0].as_shape()
self.assertEqual(aw.drawing.ShapeType.IMAGE, shape.shape_type)
# العقدة الثانية من نوع Shape هي AutoShape نفسها.
shape = shapes[1].as_shape()
self.assertEqual(aw.drawing.ShapeType.CAN, shape.shape_type)
# العقدة الثالثة من نوع Shape هي ما كان حقل EMBED الذي احتوى جدول البيانات الخارجي.
shape = shapes[2].as_shape()
self.assertEqual(aw.drawing.ShapeType.OLE_OBJECT, shape.shape_type)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldShape](../)

