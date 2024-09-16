---
title: HtmlInsertOptions enumeration
linktitle: HtmlInsertOptions enumeration
articleTitle: HtmlInsertOptions enumeration
second_title: Aspose.Words for Python
description: "aspose.words.HtmlInsertOptions enumeration. Specifies options for the [DocumentBuilder.insert_html()](../documentbuilder/insert_html/#str_htmlinsertoptions) method."
type: docs
weight: 490
url: /python-net/aspose.words/htmlinsertoptions/
---

## HtmlInsertOptions enumeration

Specifies options for the [DocumentBuilder.insert_html()](../documentbuilder/insert_html/#str_htmlinsertoptions) method.



### Members

| Name | Description |
| --- | --- |
| NONE | Use the default options when inserting HTML. |
| USE_BUILDER_FORMATTING | Use font and paragraph formatting specified in [DocumentBuilder](../documentbuilder/) as base formatting for text inserted from HTML. |
| REMOVE_LAST_EMPTY_PARAGRAPH | Remove the empty paragraph that is normally inserted after HTML that ends with a block-level element. |
| PRESERVE_BLOCKS | Preserve properties of block-level elements. |

### Examples

Shows how to allows better preserve borders and margins seen.

```python
html = "\n                <html>\n                    <div style='border:dotted'>\n                    <div style='border:solid'>\n                        <p>paragraph 1</p>\n                        <p>paragraph 2</p>\n                    </div>\n                    </div>\n                </html>"
# Set the new mode of import HTML block-level elements.
insert_options = aw.HtmlInsertOptions.PRESERVE_BLOCKS
builder = aw.DocumentBuilder()
builder.insert_html(html=html, options=insert_options)
builder.document.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.PreserveBlocks.docx')
```

### See Also

* module [aspose.words](../)

