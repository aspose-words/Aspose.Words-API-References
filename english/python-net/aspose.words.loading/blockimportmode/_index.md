---
title: BlockImportMode enumeration
linktitle: BlockImportMode enumeration
articleTitle: BlockImportMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.loading.BlockImportMode enumeration. Specifies how properties of block-level elements are imported from HTML-based documents."
type: docs
weight: 10
url: /python-net/aspose.words.loading/blockimportmode/
---

## BlockImportMode enumeration

Specifies how properties of block-level elements are imported from HTML-based documents.


### Members

| Name | Description |
| --- | --- |
| MERGE | Properties of parent blocks are merged and stored on child elements (i.e. paragraphs or tables). |
| PRESERVE | Properties of parent blocks are imported to a special logical structure and are stored separately from document nodes. |

### Examples

Shows how properties of block-level elements are imported from HTML-based documents.

```python
html = "\n            <html>\n                <div style='border:dotted'>\n                    <div style='border:solid'>\n                        <p>paragraph 1</p>\n                        <p>paragraph 2</p>\n                    </div>\n                </div>\n            </html>"
stream = io.BytesIO(system_helper.text.Encoding.get_bytes(html, system_helper.text.Encoding.utf_8()))
load_options = aw.loading.HtmlLoadOptions()
# Set the new mode of import HTML block-level elements.
load_options.block_import_mode = block_import_mode
doc = aw.Document(stream=stream, load_options=load_options)
doc.save(file_name=ARTIFACTS_DIR + 'HtmlLoadOptions.BlockImport.docx')
```

### See Also

* module [aspose.words.loading](../)

