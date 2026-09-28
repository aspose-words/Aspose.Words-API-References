---
title: EndnoteOptions.position property
linktitle: position property
articleTitle: position property
second_title: Aspose.Words for Python
description: "EndnoteOptions.position property. Specifies the endnotes position."
type: docs
weight: 20
url: /ar/python-net/aspose.words.notes/endnoteoptions/position/
---

## EndnoteOptions.position property

Specifies the endnotes position.


```python
@property
def position(self) -> aspose.words.notes.EndnotePosition:
    ...

@position.setter
def position(self, value: aspose.words.notes.EndnotePosition):
    ...

```

### Examples

Shows how to select a different place where the document collects and displays its endnotes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# الحاشية الختامية هي طريقة لإرفاق مرجع أو تعليق جانبي بالنص
# الذي لا يتداخل مع تدفق النص الأساسي.
# إدراج حاشية ختامية يضيف رمز مرجع صغير مرتفع.
# في النص الأساسي حيث نقوم بإدراج الحاشية الختامية.
# كل حاشية ختامية تنشئ أيضًا مدخلاً في نهاية المستند، يتكون من رمز
# يتطابق مع رمز المرجع في النص الأساسي.
# نص المرجع الذي نمرره إلى طريقة "InsertEndnote" في منشئ المستند.
builder.write('Hello world!')
builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text='Endnote contents.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('This is the second section.')
# يمكننا استخدام خاصية "Position" لتحديد المكان الذي سيضع فيه المستند جميع الحواشي الختامية.
# إذا قمنا بتعيين قيمة خاصية "Position" إلى "EndnotePosition.EndOfDocument",
# ستظهر كل حاشية سفلية في مجموعة في نهاية المستند. هذه هي القيمة الافتراضية.
# إذا قمنا بتعيين قيمة خاصية "Position" إلى "EndnotePosition.EndOfSection",
# سيظهر كل حاشية سفلية في مجموعة في نهاية القسم الذي يحتوي نصه على علامة الإشارة للحاشية الختامية.
doc.endnote_options.position = endnote_position
doc.save(file_name=ARTIFACTS_DIR + 'InlineStory.PositionEndnote.docx')
```

### See Also

* module [aspose.words.notes](../../)
* class [EndnoteOptions](../)

