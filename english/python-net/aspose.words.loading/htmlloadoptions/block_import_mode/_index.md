---
title: HtmlLoadOptions.block_import_mode property
linktitle: block_import_mode property
articleTitle: block_import_mode property
second_title: Aspose.Words for Python
description: "HtmlLoadOptions.block_import_mode property. Gets or sets a value that specifies how properties of block-level elements are imported"
type: docs
weight: 20
url: /python-net/aspose.words.loading/htmlloadoptions/block_import_mode/
---

## HtmlLoadOptions.block_import_mode property

Gets or sets a value that specifies how properties of block-level elements are imported.
Default value is [BlockImportMode.MERGE](../../blockimportmode/#MERGE).



```python
@property
def block_import_mode(self) -> aspose.words.loading.BlockImportMode:
    ...

@block_import_mode.setter
def block_import_mode(self, value: aspose.words.loading.BlockImportMode):
    ...

```

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

* module [aspose.words.loading](../../)
* class [HtmlLoadOptions](../)

