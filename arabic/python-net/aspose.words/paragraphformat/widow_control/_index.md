---
title: ParagraphFormat.widow_control property
linktitle: widow_control property
articleTitle: widow_control property
second_title: Aspose.Words for Python
description: "ParagraphFormat.widow_control property. True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph."
type: docs
weight: 410
url: /ar/python-net/aspose.words/paragraphformat/widow_control/
---

## ParagraphFormat.widow_control property

True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph.


```python
@property
def widow_control(self) -> bool:
    ...

@widow_control.setter
def widow_control(self, value: bool):
    ...

```

### Examples

Shows how to enable widow/orphan control for a paragraph.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# عند كتابة نص لا يتسع في صفحة واحدة، قد ينتقل سطر واحد إلى الصفحة التالية.
# السطر الوحيد الذي ينتقل إلى الصفحة التالية يُسمى "Orphan",
# والسطر السابق الذي انقطع عنده الـ "Orphan" يُسمى "Widow".
# يمكننا إصلاح الـ Orphans والـ Widows بإعادة ترتيب النص عبر حجم الخط أو التباعد أو هوامش الصفحة.
# إذا أردنا الحفاظ على أبعاد المستند، يمكننا ضبط هذه العلامة إلى "true"
# لإدراج الـ Widows في نفس الصفحة مع الـ Orphans الخاصة بها.
# ترك هذه العلامة على "false" سيترك أزواج widow/orphan في النص.
# كل فقرة لديها هذا الإعداد المتاح في Microsoft Word عبر Home -> Paragraph -> Paragraph Settings
# (زر في الزاوية السفلية اليمنى من علامة تبويب "Paragraph") -> "Widow/Orphan control".
builder.paragraph_format.widow_control = widow_control
# أدرج نصًا ينتج عنه orphan و widow.
builder.font.size = 68
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.WidowControl.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

