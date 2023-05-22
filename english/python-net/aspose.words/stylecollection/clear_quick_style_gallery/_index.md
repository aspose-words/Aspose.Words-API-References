---
title: StyleCollection.clear_quick_style_gallery method
linktitle: clear_quick_style_gallery method
articleTitle: clear_quick_style_gallery method
second_title: Aspose.Words for Python
description: "StyleCollection.clear_quick_style_gallery method. Removes all styles from the Quick Style Gallery panel."
type: docs
weight: 80
url: /python-net/aspose.words/stylecollection/clear_quick_style_gallery/
---

## clear_quick_style_gallery() {#default}

Removes all styles from the Quick Style Gallery panel.


```python
def clear_quick_style_gallery(self):
    ...
```

### Examples

Shows how to remove styles from Style Gallery panel.

```python
doc = aw.Document()

# Note that remove styles work only with DOCX format for now.
doc.styles.clear_quick_style_gallery()

doc.save(ARTIFACTS_DIR + "Styles.remove_styles_from_style_gallery.docx")
```

### See Also

* module [aspose.words](../../)
* class [StyleCollection](../)

