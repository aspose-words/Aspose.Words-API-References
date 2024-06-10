---
title: ImportFormatOptions.merge_pasted_lists property
linktitle: merge_pasted_lists property
articleTitle: merge_pasted_lists property
second_title: Aspose.Words for Python
description: "ImportFormatOptions.merge_pasted_lists property. Gets or sets a boolean value that specifies whether pasted lists will be merged with surrounding lists"
type: docs
weight: 70
url: /python-net/aspose.words/importformatoptions/merge_pasted_lists/
---

## ImportFormatOptions.merge_pasted_lists property

Gets or sets a boolean value that specifies whether pasted lists will be merged with surrounding lists.
The default value is ``False``.



```python
@property
def merge_pasted_lists(self) -> bool:
    ...

@merge_pasted_lists.setter
def merge_pasted_lists(self, value: bool):
    ...

```

### Examples

Shows how to merge lists from a documents.

```python
src_doc = aw.Document(file_name=MY_DIR + 'List item.docx')
dst_doc = aw.Document(file_name=MY_DIR + 'List destination.docx')
options = aw.ImportFormatOptions()
options.merge_pasted_lists = True
# Set the "MergePastedLists" property to "true" pasted lists will be merged with surrounding lists.
dst_doc.append_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.USE_DESTINATION_STYLES, import_format_options=options)
dst_doc.save(file_name=ARTIFACTS_DIR + 'Document.MergePastedLists.docx')
```

### See Also

* module [aspose.words](../../)
* class [ImportFormatOptions](../)

