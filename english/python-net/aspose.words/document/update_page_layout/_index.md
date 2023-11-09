---
title: Document.update_page_layout method
linktitle: update_page_layout method
articleTitle: update_page_layout method
second_title: Aspose.Words for Python
description: "Document.update_page_layout method. Rebuilds the page layout of the document."
type: docs
weight: 740
url: /python-net/aspose.words/document/update_page_layout/
---

## update_page_layout() {#default}

Rebuilds the page layout of the document.


```python
def update_page_layout(self):
    ...
```

### Remarks

This method formats a document into pages and updates the page number related fields in the document such
as PAGE, PAGES, PAGEREF and REF. The up-to-date page layout information is required for a correct rendering of the document
to fixed-page formats.

This method is automatically invoked when you first convert a document to PDF, XPS, image or print it.
However, if you modify the document after rendering and then attempt to render it again - Aspose.Words will not
update the page layout automatically. In this case you should call [Document.update_page_layout()](./#default) before
rendering again.




### Examples

Shows when to recalculate the page layout of the document.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

# Saving a document to PDF, to an image, or printing for the first time will automatically
# cache the layout of the document within its pages.
doc.save(ARTIFACTS_DIR + "Document.update_page_layout.1.pdf")

# Modify the document in some way.
doc.styles.get_by_name("Normal").font.size = 6
doc.sections[0].page_setup.orientation = aw.Orientation.LANDSCAPE
doc.sections[0].page_setup.margins = aw.Margins.MIRRORED

# In the current version of Aspose.Words, modifying the document does not automatically rebuild
# the cached page layout. If we wish for the cached layout
# to stay up to date, we will need to update it manually.
doc.update_page_layout()

doc.save(ARTIFACTS_DIR + "Document.update_page_layout.2.pdf")
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

