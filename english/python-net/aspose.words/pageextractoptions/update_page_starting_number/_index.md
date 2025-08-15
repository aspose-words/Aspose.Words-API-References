---
title: PageExtractOptions.update_page_starting_number property
linktitle: update_page_starting_number property
articleTitle: update_page_starting_number property
second_title: Aspose.Words for Python
description: "PageExtractOptions.update_page_starting_number property. Specifies whether the start page number in the resulting document shall be updated"
type: docs
weight: 30
url: /python-net/aspose.words/pageextractoptions/update_page_starting_number/
---

## PageExtractOptions.update_page_starting_number property

Specifies whether the start page number in the resulting document shall be updated.
Default value is ``True``.



```python
@property
def update_page_starting_number(self) -> bool:
    ...

@update_page_starting_number.setter
def update_page_starting_number(self, value: bool):
    ...

```

### Examples

Show how to reset the initial page numbering and save the NUMPAGE field.

```python
doc = aw.Document(file_name=MY_DIR + 'Page fields.docx')
# Default behavior:
# The extracted page numbering is the same as in the original document, as if we had selected "Print 2 pages" in MS Word.
# The start page will be set to 2 and the field indicating the number of pages will be removed
# and replaced with a constant value equal to the number of pages.
extracted_doc1 = doc.extract_pages(index=1, count=1)
extracted_doc1.save(file_name=ARTIFACTS_DIR + 'Document.ExtractPagesWithOptions.Default.docx')
# Altered behavior:
# The extracted page numbering is reset and a new one begins,
# as if we had copied the contents of the second page and pasted it into a new document.
# The start page will be set to 1 and the field indicating the number of pages will be left unchanged
# and will show the current number of pages.
extract_options = aw.PageExtractOptions()
extract_options.update_page_starting_number = False
extract_options.unlink_pages_number_fields = False
extracted_doc2 = doc.extract_pages(index=1, count=1, options=extract_options)
extracted_doc2.save(file_name=ARTIFACTS_DIR + 'Document.ExtractPagesWithOptions.Options.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageExtractOptions](../)

