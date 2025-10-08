---
title: PdfSaveOptions.page_layout property
linktitle: page_layout property
articleTitle: page_layout property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.page_layout property. Specifies the page layout to be used when the document is opened in a PDF reader."
type: docs
weight: 260
url: /python-net/aspose.words.saving/pdfsaveoptions/page_layout/
---

## PdfSaveOptions.page_layout property

Specifies the page layout to be used when the document is opened in a PDF reader.


```python
@property
def page_layout(self) -> aspose.words.saving.PdfPageLayout:
    ...

@page_layout.setter
def page_layout(self, value: aspose.words.saving.PdfPageLayout):
    ...

```

### Remarks

The default value is [PdfPageLayout.SINGLE_PAGE](../../pdfpagelayout/#SINGLE_PAGE).



### Examples

Shows how to display pages when opened in a PDF reader.

```python
doc = aw.Document(file_name=MY_DIR + 'Big document.docx')
# Display the pages two at a time, with odd-numbered pages on the left.
save_options = aw.saving.PdfSaveOptions()
save_options.page_layout = aw.saving.PdfPageLayout.TWO_PAGE_LEFT
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.PageLayout.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

