---
title: FixedPageSaveOptions.optimize_output property
linktitle: optimize_output property
articleTitle: optimize_output property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.optimize_output property. Flag indicates whether it is required to optimize output"
type: docs
weight: 50
url: /python-net/aspose.words.saving/fixedpagesaveoptions/optimize_output/
---

## FixedPageSaveOptions.optimize_output property

Flag indicates whether it is required to optimize output.
If this flag is set redundant nested canvases and empty canvases are removed,
also neighbor glyphs with the same formatting are concatenated.
Note: The accuracy of the content display may be affected if this property is set to ``True``.

Default is ``False``.



### Examples

Shows how to optimize document objects while saving to xps.

```python
doc = aw.Document(MY_DIR + "Unoptimized document.docx")

# Create an "XpsSaveOptions" object to pass to the document's "save" method
# to modify how that method converts the document to .XPS.
save_options = aw.saving.XpsSaveOptions()

# Set the "optimize_output" property to "True" to take measures such as removing nested or empty canvases
# and concatenating adjacent runs with identical formatting to optimize the output document's content.
# This may affect the appearance of the document.
# Set the "optimize_output" property to "False" to save the document normally.
save_options.optimize_output = optimize_output

doc.save(ARTIFACTS_DIR + "XpsSaveOptions.optimize_output.xps", save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

