---
title: Document.footnote_options property
linktitle: footnote_options property
articleTitle: footnote_options property
second_title: Aspose.Words for Python
description: "Document.footnote_options property. Provides options that control numbering and positioning of footnotes in this document."
type: docs
weight: 160
url: /ar/python-net/aspose.words/document/footnote_options/
---

## Document.footnote_options property

Provides options that control numbering and positioning of footnotes in this document.


```python
@property
def footnote_options(self) -> aspose.words.notes.FootnoteOptions:
    ...

```

### Examples

Shows how to select a different place where the document collects and displays its footnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# الحاشية السفلية هي طريقة لإرفاق إشارة أو تعليق جانبي إلى النص.
# الذي لا يتداخل مع تدفق النص الأساسي.
# إدراج حاشية سفلية يضيف رمز إشارة صغير مرتفع.
# في نص الجسم الرئيسي حيث نقوم بإدراج الحاشية السفلية.
# كل حاشية سفلية تنشئ أيضًا مدخلاً في أسفل الصفحة، يتكون من رمز.
# يتطابق مع رمز المرجع في النص الأساسي.
# نص الإشارة الذي نمرره إلى طريقة "InsertFootnote" في مُنشئ المستند.
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote contents.')
# يمكننا استخدام الخاصية "Position" لتحديد المكان الذي سيضع فيه المستند جميع الحواشي السفلية.
# إذا قمنا بتعيين قيمة الخاصية "Position" إلى "FootnotePosition.BottomOfPage",
# ستظهر كل حاشية سفلية في أسفل الصفحة التي تحتوي على علامة الإشارة الخاصة بها. هذه هي القيمة الافتراضية.
# إذا قمنا بتعيين قيمة الخاصية "Position" إلى "FootnotePosition.BeneathText",
# ستظهر كل حاشية سفلية في نهاية نص الصفحة الذي يحتوي على علامة الإشارة الخاصة بها.
doc.footnote_options.position = footnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionFootnote.docx')
```

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

Shows how to restart footnote/endnote numbering at certain places in the document.

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
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 3.')
builder.write('Text 4. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.FOOTNOTE, footnote_text='Footnote 4.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.write('Text 1. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 1.')
builder.write('Text 2. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 2.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Text 3. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 3.')
builder.write('Text 4. ')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote 4.')
# بشكل افتراضي، رمز الإشارة لكل حاشية سفلية وحاشية ختامية هو فهرسها.
# بين جميع الحواشي السفلية/الختامية في المستند. كل مستند يحتفظ بعدّات منفصلة
# للحواشي السفلية والختامية ولا يعيد تشغيل هذه العدّات في أي نقطة.
self.assertEqual(doc.footnote_options.restart_rule, aw.notes.FootnoteNumberingRule.DEFAULT)
self.assertEqual(aw.notes.FootnoteNumberingRule.DEFAULT, aw.notes.FootnoteNumberingRule.CONTINUOUS)
# يمكننا استخدام الخاصية "RestartRule" لجعل المستند يعيد التشغيل
# عدد الحواشي/الحواشي الختامية يبدأ في صفحة أو قسم جديد.
doc.footnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_PAGE
doc.endnote_options.restart_rule = aw.notes.FootnoteNumberingRule.RESTART_SECTION
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.NumberingRule.docx')
```

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

* module [aspose.words](../../)
* class [Document](../)

