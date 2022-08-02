---
title: font_format property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets [ExportFontFormat](../../exportfontformat/) used for font exporting"
type: docs
weight: 90
url: /python-net/aspose.words.saving/htmlfixedsaveoptions/font_format/
---

## HtmlFixedSaveOptions.font_format property

Gets or sets [ExportFontFormat](../../exportfontformat/) used for font exporting.
Default value is [ExportFontFormat.WOFF](../../exportfontformat/#WOFF).



### Examples

Shows how use fonts only from the target machine when saving a document to HTML.

```python
doc = aw.Document(MY_DIR + "Bullet points with alternative font.docx")

save_options = aw.saving.HtmlFixedSaveOptions()
save_options.export_embedded_css = True
save_options.use_target_machine_fonts = use_target_machine_fonts
save_options.font_format = aw.saving.ExportFontFormat.TTF
save_options.export_embedded_fonts = False

doc.save(ARTIFACTS_DIR + "HtmlFixedSaveOptions.using_machine_fonts.html", save_options)

with open(ARTIFACTS_DIR + "HtmlFixedSaveOptions.using_machine_fonts.html", "rt", encoding="utf-8") as file:
    out_doc_contents = file.read()

if use_target_machine_fonts:
    self.assertNotRegex(out_doc_contents, "@font-face")
else:
    self.assertIn(
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local('☺'), " +
        "url('HtmlFixedSaveOptions.using_machine_fonts/font001.ttf') format('truetype'); }",
        out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

