---
title: FootnoteOptions.restart_rule property
linktitle: restart_rule property
articleTitle: restart_rule property
second_title: Aspose.Words for Python
description: "FootnoteOptions.restart_rule property. Determines when automatic numbering restarts."
type: docs
weight: 40
url: /ar/python-net/aspose.words.notes/footnoteoptions/restart_rule/
---

## FootnoteOptions.restart_rule property

Determines when automatic numbering restarts.


```python
@property
def restart_rule(self) -> aspose.words.notes.FootnoteNumberingRule:
    ...

@restart_rule.setter
def restart_rule(self, value: aspose.words.notes.FootnoteNumberingRule):
    ...

```

### Examples

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

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

