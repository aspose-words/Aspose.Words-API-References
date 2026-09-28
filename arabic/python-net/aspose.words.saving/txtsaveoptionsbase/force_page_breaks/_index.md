---
title: TxtSaveOptionsBase.force_page_breaks property
linktitle: force_page_breaks property
articleTitle: force_page_breaks property
second_title: Aspose.Words for Python
description: "TxtSaveOptionsBase.force_page_breaks property. Allows to specify whether the page breaks should be preserved during export."
type: docs
weight: 30
url: /ar/python-net/aspose.words.saving/txtsaveoptionsbase/force_page_breaks/
---

## TxtSaveOptionsBase.force_page_breaks property

Allows to specify whether the page breaks should be preserved during export.

The default value is ``False``.




```python
@property
def force_page_breaks(self) -> bool:
    ...

@force_page_breaks.setter
def force_page_breaks(self, value: bool):
    ...

```

### Remarks

The property affects only page breaks that are inserted explicitly into a document. 
It is not related to page breaks that MS Word automatically inserts at the end of each page.


### Examples

Shows how to specify whether to preserve page breaks when exporting a document to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Page 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3')
# إنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى "Save" الخاص بالمستند
# طريقة لتعديل كيفية حفظ المستند كنص عادي.
save_options = aw.saving.TxtSaveOptions()
# كائنات Aspose.Words "Document" تحتوي على فواصل صفحات، مثل مستندات Microsoft Word.
# تنسيقات الحفظ مثل ".txt" هي نص مستمر واحد دون فواصل صفحات.
# اضبط الخاصية "ForcePageBreaks" إلى "true" للحفاظ على جميع فواصل الصفحات بصيغة أحرف '\f'.
# اضبط الخاصية "ForcePageBreaks" إلى "false" لتجاهل جميع فواصل الصفحات.
save_options.force_page_breaks = force_page_breaks
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PageBreaks.txt', save_options=save_options)
# إذا قمنا بتحميل مستند نص عادي يحتوي على فواصل صفحات،
# سيستخدم كائن "Document" هذه الفواصل لتقسيم النص إلى صفحات.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PageBreaks.txt')
self.assertEqual(3 if force_page_breaks else 1, doc.page_count)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptionsBase](../)

