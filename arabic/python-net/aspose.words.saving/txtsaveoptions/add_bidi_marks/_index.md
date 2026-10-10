---
title: TxtSaveOptions.add_bidi_marks property
linktitle: add_bidi_marks property
articleTitle: add_bidi_marks property
second_title: Aspose.Words for Python
description: "TxtSaveOptions.add_bidi_marks property. Specifies whether to add bi-directional marks before each BiDi run when exporting in plain text format."
type: docs
weight: 20
url: /ar/python-net/aspose.words.saving/txtsaveoptions/add_bidi_marks/
---

## TxtSaveOptions.add_bidi_marks property

Specifies whether to add bi-directional marks before each BiDi run when exporting in plain text format.

The default value is ``False``.




```python
@property
def add_bidi_marks(self) -> bool:
    ...

@add_bidi_marks.setter
def add_bidi_marks(self, value: bool):
    ...

```

### Examples

Shows how to insert Unicode Character 'RIGHT-TO-LEFT MARK' (U+200F) before each bi-directional Run in text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Hello world!')
builder.paragraph_format.bidi = True
builder.writeln('שלום עולם!')
builder.writeln('مرحبا بالعالم!')
# إنشاء كائن \"TxtSaveOptions\"، والذي يمكننا تمريره إلى طريقة \"save\" الخاصة بالمستند
# لتعديل طريقة حفظ المستند كنص عادي.
save_options = aw.saving.TxtSaveOptions()
save_options.encoding = 'utf-8'
# عيّن خاصية \"add_bidi_marks\" إلى \"True\" لإضافة علامات قبل المقاطع
# مع نص من اليمين إلى اليسار للإشارة إلى ذلك.
# عيّن خاصية \"add_bidi_marks\" إلى \"False\" لكتابة جميع النص من اليسار إلى اليمين
# والمقاطع من اليمين إلى اليسار بنفس القدر دون أي شيء يشير إلى أيهما أي.
save_options.add_bidi_marks = add_bidi_marks
doc.save(ARTIFACTS_DIR + 'TxtSaveOptions.add_bidi_marks.txt', save_options)
with open(ARTIFACTS_DIR + 'TxtSaveOptions.add_bidi_marks.txt', 'rb') as file:
    doc_text = file.read().decode('utf-8')
if add_bidi_marks:
    self.assertEqual('\ufeffHello world!\u200e\r\nשלום עולם!\u200f\r\nمرحبا بالعالم!\u200f\r\n\r\n', doc_text)
    self.assertIn('\u200f', doc_text)
else:
    self.assertEqual('\ufeffHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n', doc_text)
    self.assertNotIn('\u200f', doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptions](../)

