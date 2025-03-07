---
title: PdfPageLayout enumeration
linktitle: PdfPageLayout enumeration
articleTitle: PdfPageLayout enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.PdfPageLayout enumeration. Specifies the page layout to be used when the document is opened in a PDF reader."
type: docs
weight: 690
url: /python-net/aspose.words.saving/pdfpagelayout/
---

## PdfPageLayout enumeration

Specifies the page layout to be used when the document is opened in a PDF reader.


### Members

| Name | Description |
| --- | --- |
| SINGLE_PAGE | Display one page at a time. |
| ONE_COLUMN | Display the pages in one column. |
| TWO_COLUMN_LEFT | Display the pages in two columns, with odd-numbered pages on the left. |
| TWO_COLUMN_RIGHT | Display the pages in two columns, with odd-numbered pages on the right. |
| TWO_PAGE_LEFT | Display the pages two at a time, with odd-numbered pages on the left. |
| TWO_PAGE_RIGHT | Display the pages two at a time, with odd-numbered pages on the right. |

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

* module [aspose.words.saving](../)

