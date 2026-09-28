---
title: FixedPageSaveOptions.page_set property
linktitle: page_set property
articleTitle: page_set property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.page_set property. Gets or sets the pages to render"
type: docs
weight: 70
url: /ar/python-net/aspose.words.saving/fixedpagesaveoptions/page_set/
---

## FixedPageSaveOptions.page_set property

Gets or sets the pages to render.
Default is all the pages in the document.


```python
@property
def page_set(self) -> aspose.words.saving.PageSet:
    ...

@page_set.setter
def page_set(self, value: aspose.words.saving.PageSet):
    ...

```

### Examples

Shows how to export Odd pages from the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 5:
    builder.writeln(f"Page {i + 1} ({('odd' if i % 2 == 0 else 'even')})")
    if i < 4:
        builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# أنشئ كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .PDF.
options = aw.saving.PdfSaveOptions()
# فيما يلي ثلاث خصائص PageSet يمكننا استخدامها لتصفية مجموعة من الصفحات من
# مستندنا لحفظها في مستند PDF ناتج بناءً على زوجية أرقام الصفحات.
# 1 - حفظ الصفحات ذات الأرقام الزوجية فقط:
options.page_set = aw.saving.PageSet.even
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportPageSet.Even.pdf', save_options=options)
# 2 - حفظ الصفحات ذات الأرقام الفردية فقط:
options.page_set = aw.saving.PageSet.odd
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportPageSet.Odd.pdf', save_options=options)
# 3 -  احفظ كل صفحة:
options.page_set = aw.saving.PageSet.all
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportPageSet.All.pdf', save_options=options)
```

Shows how to extract pages based on exact page indices.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# أضف خمس صفحات إلى المستند.
i = 1
while i < 6:
    builder.write('Page ' + str(i))
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# أنشئ كائن "XpsSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند.
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .XPS.
xps_options = aw.saving.XpsSaveOptions()
# استخدم الخاصية "PageSet" لتحديد مجموعة من صفحات المستند لحفظها في مخرجات XPS.
# في هذه الحالة، سنختار، عبر فهرس يبدأ من الصفر، ثلاث صفحات فقط: الصفحة 1، الصفحة 2، والصفحة 4.
xps_options.page_set = aw.saving.PageSet(pages=[0, 1, 3])
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.ExportExactPages.xps', save_options=xps_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

