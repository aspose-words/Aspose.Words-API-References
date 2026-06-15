---
title: IBibliographyStylesProvider class
linktitle: IBibliographyStylesProvider class
articleTitle: IBibliographyStylesProvider class
second_title: Aspose.Words for Python
description: "aspose.words.fields.IBibliographyStylesProvider class. Implement this interface to provide bibliography style for the  [FieldBibliography](../fieldbibliography/) and [FieldCitation](../fieldcitation/) fields when they're updated."
type: docs
weight: 1210
url: /python-net/aspose.words.fields/ibibliographystylesprovider/
---

## IBibliographyStylesProvider class

Implement this interface to provide bibliography style for
the  [FieldBibliography](../fieldbibliography/) and [FieldCitation](../fieldcitation/) fields when they're updated.



### Methods

| Name | Description |
| --- | --- |
|[ get_style(style_file_name)](./get_style/#str) | Returns bibliography style. |

### Examples

Shows how to override built-in styles or provide custom one (BibliographyStylesProvider).

```python
class BibliographyStylesProvider(aw.fields.IBibliographyStylesProvider):

    def get_style(self, style_file_name):
        return system_helper.io.File.open_read(MY_DIR + 'Bibliography custom style.xsl')
```

### See Also

* module [aspose.words.fields](../)

