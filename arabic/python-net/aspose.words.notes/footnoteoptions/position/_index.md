---
title: FootnoteOptions.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "FootnoteOptions.position property. Specifies the footnotes position."
type: docs
weight: 30
url: /ar/python-net/aspose.words.notes/footnoteoptions/position/
---

## FootnoteOptions.position property

Specifies the footnotes position.


```python
@property
def position(self) -> aspose.words.notes.FootnotePosition:
    ...

@position.setter
def position(self, value: aspose.words.notes.FootnotePosition):
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

### See Also

* module [aspose.words.notes](../../)
* class [FootnoteOptions](../)

