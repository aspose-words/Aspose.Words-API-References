---
title: EndnoteOptions.start_number property
linktitle: start_number property
articleTitle: start_number property
second_title: Aspose.Words for Python
description: "EndnoteOptions.start_number property. Specifies the starting number or character for the first automatically numbered endnotes."
type: docs
weight: 40
url: /ar/python-net/aspose.words.notes/endnoteoptions/start_number/
---

## EndnoteOptions.start_number property

Specifies the starting number or character for the first automatically numbered endnotes.


```python
@property
def start_number(self) -> int:
    ...

@start_number.setter
def start_number(self, value: int):
    ...

```

### Remarks

This property has effect only when [EndnoteOptions.restart_rule](../restart_rule/) is set to
[FootnoteNumberingRule.CONTINUOUS](../../footnotenumberingrule/#CONTINUOUS).




### Examples

Shows how to set a number at which the document begins the footnote/endnote count.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# الحواشي السفلية والحواشي الختامية هي طريقة لإرفاق إشارة أو تعليق جانبي إلى النص.
# الذي لا يتداخل مع تدفق النص الأساسي.
# إدراج حاشية سفلية/حاشية ختامية يضيف رمز إشارة صغير مرتفع.
# في نص الجسم الرئيسي حيث نقوم بإدراج الحاشية السفلية/الحاشية الختامية.
# كل حاشية/حاشية ختامية تنشئ أيضًا مدخلاً يتكون من رمز
# يتطابق مع رمز المرجع في النص الأساسي.
# نص المرجع الذي نمرره إلى طريقة "InsertEndnote" في منشئ المستند.
# مدخلات الحواشي السفلية، بشكل افتراضي، تظهر في أسفل كل صفحة تحتوي على
# رموز الإشارة الخاصة بها، والحواشي الختامية تظهر في نهاية المستند.
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.')
builder.insert_paragraph()
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.')
# بشكل افتراضي، رمز الإشارة لكل حاشية سفلية وحاشية ختامية هو فهرسها.
# بين جميع الحواشي السفلية/الختامية في المستند. كل مستند يحتفظ بعدّات منفصلة
# للحوامش والحواشي الختامية، حيث يبدأ كلاهما من 1.
self.assertEqual(1, doc.footnote_options.start_number)
self.assertEqual(1, doc.endnote_options.start_number)
# يمكننا استخدام الخاصية "StartNumber" لجعل المستند
# يبدأ عد الحواشي أو الحواشي الختامية برقم مختلف.
doc.endnote_options.number_style = aw.NumberStyle.ARABIC
doc.endnote_options.start_number = 50
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.StartNumber.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

