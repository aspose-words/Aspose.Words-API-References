---
title: HtmlSaveOptions.resolve_font_names property
linktitle: resolve_font_names property
articleTitle: resolve_font_names property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.resolve_font_names property. Specifies whether font family names used in the document are resolved and substituted according to [Document.font_settings](../../../aspose.words/document/font_settings/) when being written into HTML-based formats."
type: docs
weight: 430
url: /python-net/aspose.words.saving/htmlsaveoptions/resolve_font_names/
---

## HtmlSaveOptions.resolve_font_names property

Specifies whether font family names used in the document are resolved and substituted according to
[Document.font_settings](../../../aspose.words/document/font_settings/) when being written into HTML-based formats.



```python
@property
def resolve_font_names(self) -> bool:
    ...

@resolve_font_names.setter
def resolve_font_names(self, value: bool):
    ...

```

### Remarks

By default, this option is set to ``False`` and font family names are written to HTML as specified
in source documents. That is, [Document.font_settings](../../../aspose.words/document/font_settings/) are ignored and no resolution or substitution
of font family names is performed.

If this option is set to ``True``, Aspose.Words uses [Document.font_settings](../../../aspose.words/document/font_settings/) to resolve
each font family name specified in a source document into the name of an available font family, performing
font substitution as required.




### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

