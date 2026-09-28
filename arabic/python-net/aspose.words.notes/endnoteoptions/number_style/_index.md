---
title: EndnoteOptions.number_style property
linktitle: number_style property
articleTitle: number_style property
second_title: Aspose.Words for Python
description: "EndnoteOptions.number_style property. Specifies the number format for automatically numbered endnotes."
type: docs
weight: 10
url: /ar/python-net/aspose.words.notes/endnoteoptions/number_style/
---

## EndnoteOptions.number_style property

Specifies the number format for automatically numbered endnotes.


```python
@property
def number_style(self) -> aspose.words.NumberStyle:
    ...

@number_style.setter
def number_style(self, value: aspose.words.NumberStyle):
    ...

```

### Remarks

Not all number styles are applicable for this property. For the list of applicable
number styles see the Insert Footnote or Endnote dialog box in Microsoft Word. If you select
a number style that is not applicable, Microsoft Word will revert to a default value.




### Examples

Shows how to change the number style of footnote/endnote reference marks.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# الحواشي السفلية والحواشي الختامية هي طريقة لإرفاق إشارة أو تعليق جانبي إلى النص.
# الذي لا يتداخل مع تدفق النص الأساسي.
# إدراج حاشية سفلية/حاشية ختامية يضيف رمز إشارة صغير مرتفع.
# في نص الجسم الرئيسي حيث نقوم بإدراج الحاشية السفلية/الحاشية الختامية.
# كل حاشية سفلية/ختامية تنشئ أيضًا مدخلاً يتكون من رمز يطابق الإشارة
# الرمز في نص الجسم الرئيسي. نص الإشارة الذي نمرره إلى طريقة "InsertEndnote" في مُنشئ المستند.
# مدخلات الحواشي السفلية، بشكل افتراضي، تظهر في أسفل كل صفحة تحتوي على
# رموز الإشارة الخاصة بها، والحواشي الختامية تظهر في نهاية المستند.
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.', reference_mark='Custom footnote reference mark')
builder.insert_paragraph()
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.', reference_mark='Custom endnote reference mark')
# بشكل افتراضي، رمز الإشارة لكل حاشية سفلية وحاشية ختامية هو فهرسها.
# بين جميع الحواشي السفلية/الختامية في المستند. كل مستند يحتفظ بعدّات منفصلة
# للحواشي السفلية وللحواشي الختامية. بشكل افتراضي، تعرض الحواشي السفلية أرقامها باستخدام الأرقام العربية،
# والحواشي الختامية تعرض أرقامها بالأحرف الرومانية الصغيرة.
self.assertEqual(aw.NumberStyle.ARABIC, doc.footnote_options.number_style)
self.assertEqual(aw.NumberStyle.LOWERCASE_ROMAN, doc.endnote_options.number_style)
# يمكننا استخدام الخاصية "NumberStyle" لتطبيق أنماط ترقيم مخصصة على الحواشي السفلية والختامية.
# هذا لن يؤثر على الحواشي السفلية/الختامية التي لديها علامات إشارة مخصصة.
doc.footnote_options.number_style = aw.NumberStyle.UPPERCASE_ROMAN
doc.endnote_options.number_style = aw.NumberStyle.UPPERCASE_LETTER
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.RefMarkNumberStyle.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

