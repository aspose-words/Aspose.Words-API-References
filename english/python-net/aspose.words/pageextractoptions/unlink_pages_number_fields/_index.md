---
title: PageExtractOptions.unlink_pages_number_fields property
linktitle: unlink_pages_number_fields property
articleTitle: unlink_pages_number_fields property
second_title: Aspose.Words for Python
description: "PageExtractOptions.unlink_pages_number_fields property. Specifies whether NUMPAGES fields in the resulting document will be replaced with their actual resulting values"
type: docs
weight: 20
url: /python-net/aspose.words/pageextractoptions/unlink_pages_number_fields/
---

## PageExtractOptions.unlink_pages_number_fields property

Specifies whether NUMPAGES fields in the resulting document will be replaced with their actual resulting values.
Default value is ``True``.



```python
@property
def unlink_pages_number_fields(self) -> bool:
    ...

@unlink_pages_number_fields.setter
def unlink_pages_number_fields(self, value: bool):
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

