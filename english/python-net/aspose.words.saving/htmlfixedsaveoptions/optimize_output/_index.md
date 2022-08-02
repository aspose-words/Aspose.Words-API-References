---
title: optimize_output property
second_title: Aspose.Words for Python via .NET API Reference
description: "Flag indicates whether it is required to optimize output"
type: docs
weight: 100
url: /python-net/aspose.words.saving/htmlfixedsaveoptions/optimize_output/
---

## HtmlFixedSaveOptions.optimize_output property

Flag indicates whether it is required to optimize output.
If this flag is set redundant nested canvases and empty canvases are removed,
also neighbor glyphs with the same formating are concatenated.
Note: The accuracy of the content display may be affected if this property is set to true.

Default is true.


### Examples

Shows how to simplify a document when saving it to HTML by removing various redundant objects.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

save_options = aw.saving.HtmlFixedSaveOptions()
save_options.optimize_output = optimize_output

doc.save(ARTIFACTS_DIR + "HtmlFixedSaveOptions.optimize_graphics_output.html", save_options)

# The size of the optimized version of the document is almost a third of the size of the unoptimized document.
if optimize_output:
    self.assertAlmostEqual(62521,
        os.path.getsize(ARTIFACTS_DIR + "HtmlFixedSaveOptions.optimize_graphics_output.html"), delta=200)
else:
    self.assertAlmostEqual(191770,
        os.path.getsize(ARTIFACTS_DIR + "HtmlFixedSaveOptions.optimize_graphics_output.html"), delta=200)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

