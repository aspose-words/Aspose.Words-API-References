---
title: ParagraphFormat.bidi property
linktitle: bidi property
articleTitle: bidi property
second_title: Aspose.Words for Python
description: "ParagraphFormat.bidi property. Gets or sets whether this is a right-to-left paragraph."
type: docs
weight: 50
url: /ar/python-net/aspose.words/paragraphformat/bidi/
---

## ParagraphFormat.bidi property

Gets or sets whether this is a right-to-left paragraph.


```python
@property
def bidi(self) -> bool:
    ...

@bidi.setter
def bidi(self, value: bool):
    ...

```

### Remarks

When ``True``, the runs and other inline objects in this paragraph
are laid out right to left.




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

Shows how to detect plaintext document text direction.

```python
# أنشئ كائن "TxtLoadOptions"، الذي يمكننا تمريره إلى مُنشئ المستند
# لتعديل طريقة تحميل مستند نص عادي.
load_options = aw.loading.TxtLoadOptions()
# قم بتعيين خاصية "DocumentDirection" إلى "DocumentDirection.Auto" لتكتشف تلقائيًا
# اتجاه كل فقرة نصية تقوم Aspose.Words بتحميلها من النص العادي.
# ستخزن خاصية "Bidi" لكل فقرة اتجاهها.
load_options.document_direction = aw.loading.DocumentDirection.AUTO
# اكتشف النص العبري من اليمين إلى اليسار.
doc = aw.Document(file_name=MY_DIR + 'Hebrew text.txt', load_options=load_options)
self.assertTrue(doc.first_section.body.first_paragraph.paragraph_format.bidi)
# اكتشف النص الإنجليزي من اليمين إلى اليسار.
doc = aw.Document(file_name=MY_DIR + 'English text.txt', load_options=load_options)
self.assertFalse(doc.first_section.body.first_paragraph.paragraph_format.bidi)
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

