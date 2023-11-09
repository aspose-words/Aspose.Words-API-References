---
title: HtmlFixedSaveOptions.export_embedded_svg property
linktitle: export_embedded_svg property
articleTitle: export_embedded_svg property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.export_embedded_svg property. Specifies whether SVG resources should be embedded into Html document"
type: docs
weight: 70
url: /python-net/aspose.words.saving/htmlfixedsaveoptions/export_embedded_svg/
---

## HtmlFixedSaveOptions.export_embedded_svg property

Specifies whether SVG resources should be embedded into Html document.
Default value is ``True``.



```python
@property
def export_embedded_svg(self) -> bool:
    ...

@export_embedded_svg.setter
def export_embedded_svg(self, value: bool):
    ...

```

### Examples

Shows how to determine where to store SVG objects when exporting a document to Html.

```python
doc = aw.Document(MY_DIR + "Images.docx")

# When we export a document with SVG objects to .html,
# Aspose.Words can place these objects in two possible locations.
# Setting the "export_embedded_svg" flag to "True" will embed all SVG object raw data
# within the output HTML, inside <image> tags.
# Setting this flag to "False" will create a file in the local file system for each SVG object.
# The HTML will link to each file using the "data" attribute of an <object> tag.
html_fixed_save_options = aw.saving.HtmlFixedSaveOptions()
html_fixed_save_options.export_embedded_svg = export_svgs

doc.save(ARTIFACTS_DIR + "HtmlFixedSaveOptions.export_embedded_svgs.html", html_fixed_save_options)

with open(ARTIFACTS_DIR + "HtmlFixedSaveOptions.export_embedded_svgs.html", "rt", encoding="utf-8") as file:
    out_doc_contents = file.read()

if export_svgs:
    self.assertFalse(os.path.exists(ARTIFACTS_DIR + "HtmlFixedSaveOptions.export_embedded_svgs/svg001.svg"))
    self.assertRegex(out_doc_contents, '<image id="image004" xlink:href=.+/>')
else:
    self.assertTrue(os.path.exists(ARTIFACTS_DIR + "HtmlFixedSaveOptions.export_embedded_svgs/svg001.svg"))
    self.assertRegex(out_doc_contents,
        '<object type="image/svg[+]xml" data="HtmlFixedSaveOptions.export_embedded_svgs/svg001[.]svg"></object>')
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

