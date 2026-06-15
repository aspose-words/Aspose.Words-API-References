---
title: TxtSaveOptionsBase.force_page_breaks property
linktitle: force_page_breaks property
articleTitle: force_page_breaks property
second_title: Aspose.Words for Python
description: "TxtSaveOptionsBase.force_page_breaks property. Allows to specify whether the page breaks should be preserved during export."
type: docs
weight: 30
url: /python-net/aspose.words.saving/txtsaveoptionsbase/force_page_breaks/
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
# Create a "TxtSaveOptions" object, which we can pass to the document's "Save"
# method to modify how we save the document to plaintext.
save_options = aw.saving.TxtSaveOptions()
# The Aspose.Words "Document" objects have page breaks, just like Microsoft Word documents.
# Save formats such as ".txt" are one continuous body of text without page breaks.
# Set the "ForcePageBreaks" property to "true" to preserve all page breaks in the form of '\f' characters.
# Set the "ForcePageBreaks" property to "false" to discard all page breaks.
save_options.force_page_breaks = force_page_breaks
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PageBreaks.txt', save_options=save_options)
# If we load a plaintext document with page breaks,
# the "Document" object will use them to split the body into pages.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PageBreaks.txt')
self.assertEqual(3 if force_page_breaks else 1, doc.page_count)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptionsBase](../)

