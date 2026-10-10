---
title: FixedPageSaveOptions.optimize_output property
linktitle: optimize_output property
articleTitle: optimize_output property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.optimize_output property. Flag indicates whether it is required to optimize output"
type: docs
weight: 50
url: /ar/python-net/aspose.words.saving/fixedpagesaveoptions/optimize_output/
---

## FixedPageSaveOptions.optimize_output property

Flag indicates whether it is required to optimize output.
If this flag is set redundant nested canvases and empty canvases are removed,
also neighbor glyphs with the same formatting are concatenated.
Note: The accuracy of the content display may be affected if this property is set to ``True``.

Default is ``False``.



```python
@property
def optimize_output(self) -> bool:
    ...

@optimize_output.setter
def optimize_output(self, value: bool):
    ...

```

### Examples

Shows how to optimize document objects while saving to xps.

```python
doc = aw.Document(file_name=MY_DIR + 'Unoptimized document.docx')
# إنشاء كائن "XpsSaveOptions" لتمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل طريقة تحويل تلك الطريقة للمستند إلى .XPS.
save_options = aw.saving.XpsSaveOptions()
# اضبط الخاصية "OptimizeOutput" إلى "true" لاتخاذ إجراءات مثل إزالة القماشات المتداخلة أو الفارغة
# ودمج المقاطع المتجاورة ذات التنسيق المتطابق لتحسين محتوى المستند الناتج.
# قد يؤثر ذلك على مظهر المستند.
# اضبط الخاصية "OptimizeOutput" إلى "false" لحفظ المستند بشكل طبيعي.
save_options.optimize_output = optimize_output
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.OptimizeOutput.xps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

