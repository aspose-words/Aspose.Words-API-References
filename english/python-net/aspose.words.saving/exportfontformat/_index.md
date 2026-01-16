---
title: ExportFontFormat enumeration
linktitle: ExportFontFormat enumeration
articleTitle: ExportFontFormat enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.ExportFontFormat enumeration. Indicates the format that is used to export fonts while rendering to HTML fixed format."
type: docs
weight: 170
url: /python-net/aspose.words.saving/exportfontformat/
---

## ExportFontFormat enumeration

Indicates the format that is used to export fonts while rendering to HTML fixed format.


### Members

| Name | Description |
| --- | --- |
| WOFF | WOFF (Web Open Font Format). |
| TTF | TTF (TrueType Font format). |

### Examples

Shows how use fonts only from the target machine when saving a document to HTML.

```python
doc = aw.Document(MY_DIR + 'Bullet points with alternative font.docx')
save_options = aw.saving.HtmlFixedSaveOptions()
save_options.export_embedded_css = True
save_options.use_target_machine_fonts = use_target_machine_fonts
save_options.font_format = aw.saving.ExportFontFormat.TTF
save_options.export_embedded_fonts = False
doc.save(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.using_machine_fonts.html', save_options)
with open(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.using_machine_fonts.html', 'rt', encoding='utf-8') as file:
    out_doc_contents = file.read()
if use_target_machine_fonts:
    self.assertNotRegex(out_doc_contents, '@font-face')
else:
    self.assertIn("@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local('☺'), " + "url('HtmlFixedSaveOptions.using_machine_fonts/font001.ttf') format('truetype'); }", out_doc_contents)
```

### See Also

* module [aspose.words.saving](../)
* property [HtmlFixedSaveOptions.font_format](../htmlfixedsaveoptions/font_format/)

