---
title: HtmlFixedSaveOptions.optimize_output property
linktitle: optimize_output property
articleTitle: optimize_output property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.optimize_output property. Flag indicates whether it is required to optimize output"
type: docs
weight: 110
url: /python-net/aspose.words.saving/htmlfixedsaveoptions/optimize_output/
---

## HtmlFixedSaveOptions.optimize_output property

Flag indicates whether it is required to optimize output.
If this flag is set redundant nested canvases and empty canvases are removed,
also neighbor glyphs with the same formating are concatenated.
Note: The accuracy of the content display may be affected if this property is set to ``True``.

Default is ``True``.



```python
@property
def optimize_output(self) -> bool:
    ...

@optimize_output.setter
def optimize_output(self, value: bool):
    ...

```

### Examples

Shows how to simplify a document when saving it to HTML by removing various redundant objects.

```python
doc = aw.Document(MY_DIR + 'Rendering.docx')
save_options = aw.saving.HtmlFixedSaveOptions()
save_options.optimize_output = optimize_output
doc.save(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.optimize_graphics_output.html', save_options)
# The size of the optimized version of the document is almost a third of the size of the unoptimized document.
if optimize_output:
    self.assertAlmostEqual(61860, os.path.getsize(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.optimize_graphics_output.html'), delta=200)
else:
    self.assertAlmostEqual(191770, os.path.getsize(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.optimize_graphics_output.html'), delta=200)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

