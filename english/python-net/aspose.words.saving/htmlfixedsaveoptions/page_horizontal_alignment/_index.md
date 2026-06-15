---
title: HtmlFixedSaveOptions.page_horizontal_alignment property
linktitle: page_horizontal_alignment property
articleTitle: page_horizontal_alignment property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.page_horizontal_alignment property. Specifies the horizontal alignment of pages in an HTML document"
type: docs
weight: 120
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
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
html_fixed_save_options = aw.saving.HtmlFixedSaveOptions()
html_fixed_save_options.page_horizontal_alignment = page_horizontal_alignment
doc.save(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.HorizontalAlignment.html', save_options=html_fixed_save_options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.HorizontalAlignment/styles.css')
switch_condition = page_horizontal_alignment
if switch_condition == aw.saving.HtmlFixedPageHorizontalAlignment.CENTER:
    assert re.search('\\.awpage \\{ position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; \\}', out_doc_contents)
elif switch_condition == aw.saving.HtmlFixedPageHorizontalAlignment.LEFT:
    assert re.search('\\.awpage \\{ position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; \\}', out_doc_contents)
elif switch_condition == aw.saving.HtmlFixedPageHorizontalAlignment.RIGHT:
    assert re.search('\\.awpage \\{ position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; \\}', out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

