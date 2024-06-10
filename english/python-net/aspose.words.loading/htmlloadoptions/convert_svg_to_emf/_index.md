---
title: HtmlLoadOptions.convert_svg_to_emf property
linktitle: convert_svg_to_emf property
articleTitle: convert_svg_to_emf property
second_title: Aspose.Words for Python
description: "HtmlLoadOptions.convert_svg_to_emf property. Gets or sets a value indicating whether to convert loaded SVG images to the EMF format"
type: docs
weight: 30
url: /python-net/aspose.words.loading/htmlloadoptions/convert_svg_to_emf/
---

## HtmlLoadOptions.convert_svg_to_emf property

Gets or sets a value indicating whether to convert loaded SVG images to the EMF format.
Default value is ``False`` and, if possible, loaded SVG images are stored as is without conversion.



```python
@property
def convert_svg_to_emf(self) -> bool:
    ...

@convert_svg_to_emf.setter
def convert_svg_to_emf(self, value: bool):
    ...

```

### Remarks

Newer versions of MS Word support SVG images natively. If the MS Word version specified in load options supports
SVG, Aspose.Words will store SVG images as is without conversion. If SVG is not supported, loaded SVG images will be
converted to the EMF format.

If, however, this option is set to ``True``, Aspose.Words will convert loaded SVG images to EMF even if SVG
images are supported by the specified version of MS Word.





### Examples

Shows how to convert SVG objects to a different format when saving HTML documents.

```python
html = "\n                    <html>\n                        <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>\n                            <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>\n                        </svg>\n                    </html>\n                    "
# Use 'convert_svg_to_emf' to turn back the legacy behavior
# where all SVG images loaded from an HTML document were converted to EMF.
# Now SVG images are loaded without conversion
# if the MS Word version specified in load options supports SVG images natively.
load_options = aw.loading.HtmlLoadOptions()
load_options.convert_svg_to_emf = True
doc = aw.Document(io.BytesIO(html.encode('utf-8')), load_options)
# This document contains a <svg> element in the form of text.
# When we save the document to HTML, we can pass a SaveOptions object
# to determine how the saving operation handles this object.
# Setting the "metafile_format" property to "HtmlMetafileFormat.PNG" to convert it to a PNG image.
# Setting the "metafile_format" property to "HtmlMetafileFormat.SVG" preserve it as a SVG object.
# Setting the "metafile_format" property to "HtmlMetafileFormat.EMF_OR_WMF" to convert it to a metafile.
options = aw.saving.HtmlSaveOptions()
options.metafile_format = html_metafile_format
doc.save(ARTIFACTS_DIR + 'HtmlSaveOptions.metafile_format.html', options)
with open(ARTIFACTS_DIR + 'HtmlSaveOptions.metafile_format.html', 'rt', encoding='utf-8') as file:
    out_doc_contents = file.read()
if html_metafile_format == aw.saving.HtmlMetafileFormat.PNG:
    self.assertIn('<p style="margin-top:0pt; margin-bottom:0pt">' + '<img src="HtmlSaveOptions.metafile_format.001.png" width="500" height="40" alt="" ' + 'style="-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline" />' + '</p>', out_doc_contents)
elif html_metafile_format == aw.saving.HtmlMetafileFormat.SVG:
    self.assertIn('<span style="-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline">' + '<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" width="499" height="40">', out_doc_contents)
elif html_metafile_format == aw.saving.HtmlMetafileFormat.EMF_OR_WMF:
    self.assertIn('<p style="margin-top:0pt; margin-bottom:0pt">' + '<img src="HtmlSaveOptions.metafile_format.001.emf" width="500" height="40" alt="" ' + 'style="-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline" />' + '</p>', out_doc_contents)
```

### See Also

* module [aspose.words.loading](../../)
* class [HtmlLoadOptions](../)

