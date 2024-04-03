---
title: HtmlLoadOptions.support_font_face_rules property
linktitle: support_font_face_rules property
articleTitle: support_font_face_rules property
second_title: Aspose.Words for Python
description: "HtmlLoadOptions.support_font_face_rules property. Gets or sets a value indicating whether to support @font-face rules and whether to load declared fonts"
type: docs
weight: 60
url: /python-net/aspose.words.loading/htmlloadoptions/support_font_face_rules/
---

## HtmlLoadOptions.support_font_face_rules property

Gets or sets a value indicating whether to support @font-face rules and whether to load declared fonts.
Default value is ``False``.



```python
@property
def support_font_face_rules(self) -> bool:
    ...

@support_font_face_rules.setter
def support_font_face_rules(self, value: bool):
    ...

```

### Remarks

If this option is enabled, fonts declared in @font-face rules are loaded and embedded into the resulting document's
font definitions (see [DocumentBase.font_infos](../../../aspose.words/documentbase/font_infos/)). This makes the loaded fonts available for rendering but
doesn't automatically enable embedding of the fonts upon saving. In order to save the document with loaded fonts,
the [FontInfoCollection.embed_true_type_fonts](../../../aspose.words.fonts/fontinfocollection/embed_true_type_fonts/) property of the [DocumentBase.font_infos](../../../aspose.words/documentbase/font_infos/)
collection should be set to ``True``.


Supported font formats are TTF, EOT, and WOFF.

@font-face rules are not supported when loading SVG images.




### Examples

Shows how to load declared "@font-face" rules.

```python
load_options = aw.loading.HtmlLoadOptions()
load_options.support_font_face_rules = True
doc = aw.Document(file_name=MY_DIR + "Html with FontFace.html", load_options=load_options)
self.assertEqual("Squarish Sans CT Regular", doc.font_infos[0].name)
```

### See Also

* module [aspose.words.loading](../../)
* class [HtmlLoadOptions](../)

