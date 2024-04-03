---
title: HtmlMetafileFormat enumeration
linktitle: HtmlMetafileFormat enumeration
articleTitle: HtmlMetafileFormat enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.HtmlMetafileFormat enumeration. Indicates the format in which metafiles are saved to HTML documents."
type: docs
weight: 250
url: /python-net/aspose.words.saving/htmlmetafileformat/
---

## HtmlMetafileFormat enumeration

Indicates the format in which metafiles are saved to HTML documents.


### Members

| Name | Description |
| --- | --- |
| PNG | Metafiles are rendered to raster PNG images. |
| SVG | Metafiles are converted to vector SVG images. |
| EMF_OR_WMF | Metafiles are saved as is, without conversion. |

### Examples

Shows how to convert SVG objects to a different format when saving HTML documents.

```python
html = """
    <html>
        <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>
            <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>
        </svg>
    </html>
    """

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

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.metafile_format.html", options)

with open(ARTIFACTS_DIR + "HtmlSaveOptions.metafile_format.html", "rt", encoding="utf-8") as file:
    out_doc_contents = file.read()

if html_metafile_format == aw.saving.HtmlMetafileFormat.PNG:
    self.assertIn(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
            "<img src=\"HtmlSaveOptions.metafile_format.001.png\" width=\"500\" height=\"40\" alt=\"\" " +
            "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
        "</p>", out_doc_contents)

elif html_metafile_format == aw.saving.HtmlMetafileFormat.SVG:
    self.assertIn(
        "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
        "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"499\" height=\"40\">",
        out_doc_contents)

elif html_metafile_format == aw.saving.HtmlMetafileFormat.EMF_OR_WMF:
    self.assertIn(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
            "<img src=\"HtmlSaveOptions.metafile_format.001.emf\" width=\"500\" height=\"40\" alt=\"\" " +
            "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
        "</p>", out_doc_contents)
```

### See Also

* module [aspose.words.saving](../)

