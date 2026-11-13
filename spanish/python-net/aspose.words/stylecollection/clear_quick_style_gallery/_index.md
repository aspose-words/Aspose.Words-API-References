---
title: StyleCollection.clear_quick_style_gallery method
linktitle: clear_quick_style_gallery method
articleTitle: clear_quick_style_gallery method
second_title: Aspose.Words for Python
description: "StyleCollection.clear_quick_style_gallery method. Removes all styles from the Quick Style Gallery panel."
type: docs
weight: 80
url: /es/python-net/aspose.words/stylecollection/clear_quick_style_gallery/
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
# Tenga en cuenta que la eliminación de estilos funciona solo con el formato DOCX por ahora.
doc.styles.clear_quick_style_gallery()
doc.save(file_name=ARTIFACTS_DIR + 'Styles.RemoveStylesFromStyleGallery.docx')
```

### See Also

* module [aspose.words](../../)
* class [StyleCollection](../)

