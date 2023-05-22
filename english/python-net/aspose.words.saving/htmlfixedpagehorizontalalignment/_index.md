---
title: HtmlFixedPageHorizontalAlignment enumeration
linktitle: HtmlFixedPageHorizontalAlignment enumeration
articleTitle: HtmlFixedPageHorizontalAlignment enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.HtmlFixedPageHorizontalAlignment enumeration. Specifies the horizontal alignment for pages in output HTML document."
type: docs
weight: 220
url: /python-net/aspose.words.saving/htmlfixedpagehorizontalalignment/
---

## HtmlFixedPageHorizontalAlignment enumeration

Specifies the horizontal alignment for pages in output HTML document.


### Members

| Name | Description |
| --- | --- |
| LEFT | Align pages to the left. |
| CENTER | Center pages. This is the default value. |
| RIGHT | Align pages to the right. |

### Examples

Shows how to set the horizontal alignment of pages when saving a document to HTML.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

html_fixed_save_options = aw.saving.HtmlFixedSaveOptions()
html_fixed_save_options.page_horizontal_alignment = page_horizontal_alignment

doc.save(ARTIFACTS_DIR + "HtmlFixedSaveOptions.horizontal_alignment.html", html_fixed_save_options)

with open(ARTIFACTS_DIR + "HtmlFixedSaveOptions.horizontal_alignment/styles.css", "rt", encoding="utf-8") as file:
    out_doc_contents = file.read()

if page_horizontal_alignment == aw.saving.HtmlFixedPageHorizontalAlignment.CENTER:
    self.assertRegex(out_doc_contents,
        "[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; }")

elif page_horizontal_alignment == aw.saving.HtmlFixedPageHorizontalAlignment.LEFT:
    self.assertRegex(out_doc_contents,
        "[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; }")

elif page_horizontal_alignment == aw.saving.HtmlFixedPageHorizontalAlignment.RIGHT:
    self.assertRegex(out_doc_contents,
        "[.]awpage { position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; }")
```

### See Also

* module [aspose.words.saving](../)

