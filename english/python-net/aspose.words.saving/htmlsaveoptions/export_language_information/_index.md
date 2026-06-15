---
title: HtmlSaveOptions.export_language_information property
linktitle: export_language_information property
articleTitle: export_language_information property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_language_information property. Specifies whether language information is exported to HTML, MHTML or EPUB"
type: docs
weight: 180
url: /python-net/aspose.words.saving/htmlsaveoptions/export_language_information/
---

## HtmlSaveOptions.export_language_information property

Specifies whether language information is exported to HTML, MHTML or EPUB.
Default is ``False``.



```python
@property
def export_language_information(self) -> bool:
    ...

@export_language_information.setter
def export_language_information(self, value: bool):
    ...

```

### Remarks

When this property is set to ``True`` Aspose.Words outputs **lang** HTML attribute on the document
elements that specify language. This can be needed to preserve language related semantics.




### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

