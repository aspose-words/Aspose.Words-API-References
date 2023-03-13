---
title: merge_pasted_lists property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets a boolean value that specifies whether pasted lists will be merged with surrounding lists"
type: docs
weight: 70
url: /python-net/aspose.words/importformatoptions/merge_pasted_lists/
---

## ImportFormatOptions.merge_pasted_lists property

Gets or sets a boolean value that specifies whether pasted lists will be merged with surrounding lists.
The default value is ``False``.



### Examples

Shows how to merge lists from a documents.

```python
src_doc = aw.Document(MY_DIR + "List item.docx")
dst_doc = aw.Document(MY_DIR + "List destination.docx")

options = aw.ImportFormatOptions()
options.merge_pasted_lists = True

# Set the "merge_pasted_lists" property to "True" pasted lists will be merged with surrounding lists.
dst_doc.append_document(src_doc, aw.ImportFormatMode.USE_DESTINATION_STYLES, options)

dst_doc.save(ARTIFACTS_DIR + "Document.merge_pasted_lists.docx")
```

### See Also

* module [aspose.words](../../)
* class [ImportFormatOptions](../)

