---
title: HtmlFixedSaveOptions.page_horizontal_alignment property
linktitle: page_horizontal_alignment property
articleTitle: page_horizontal_alignment property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.page_horizontal_alignment property. Specifies the horizontal alignment of pages in an HTML document"
type: docs
weight: 110
url: /python-net/aspose.words.saving/htmlfixedsaveoptions/page_horizontal_alignment/
---

## HtmlFixedSaveOptions.page_horizontal_alignment property

Specifies the horizontal alignment of pages in an HTML document.
Default value is [HtmlFixedPageHorizontalAlignment.CENTER](../../htmlfixedpagehorizontalalignment/#CENTER).



```python
@property
def page_horizontal_alignment(self) -> aspose.words.saving.HtmlFixedPageHorizontalAlignment:
    ...

@page_horizontal_alignment.setter
def page_horizontal_alignment(self, value: aspose.words.saving.HtmlFixedPageHorizontalAlignment):
    ...

```

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

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

