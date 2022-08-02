---
title: export_embedded_images property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies whether images should be embedded into Html document in Base64 format"
type: docs
weight: 60
url: /python-net/aspose.words.saving/htmlfixedsaveoptions/export_embedded_images/
---

## HtmlFixedSaveOptions.export_embedded_images property

Specifies whether images should be embedded into Html document in Base64 format.
Note setting this flag can significantly increase size of output Html file.


### Examples

Shows how to determine where to store images when exporting a document to Html.

```python
doc = aw.Document(MY_DIR + "Images.docx")

# When we export a document with embedded images to .html,
# Aspose.Words can place the images in two possible locations.
# Setting the "export_embedded_images" flag to "True" will store the raw data
# for all images within the output HTML document, in the "src" attribute of <image> tags.
# Setting this flag to "False" will create an image file in the local file system for every image,
# and store all these files in a separate folder.
html_fixed_save_options = aw.saving.HtmlFixedSaveOptions()
html_fixed_save_options.export_embedded_images = export_images

doc.save(ARTIFACTS_DIR + "HtmlFixedSaveOptions.export_embedded_images.html", html_fixed_save_options)

with open(ARTIFACTS_DIR + "HtmlFixedSaveOptions.export_embedded_images.html", "rt", encoding="utf-8") as file:
    out_doc_contents = file.read()

if export_images:
    self.assertFalse(os.path.exists(ARTIFACTS_DIR + "HtmlFixedSaveOptions.export_embedded_images/image001.jpeg"))
    self.assertRegex(out_doc_contents,
        '<img class="awimg" style="left:0pt; top:0pt; width:493.1pt; height:300.55pt;" src=".+" />')
else:
    self.assertTrue(os.path.exists(ARTIFACTS_DIR + "HtmlFixedSaveOptions.export_embedded_images/image001.jpeg"))
    self.assertIn(
        '<img class="awimg" style="left:0pt; top:0pt; width:493.1pt; height:300.55pt;" ' +
        'src="HtmlFixedSaveOptions.export_embedded_images/image001.jpeg" />',
        out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

