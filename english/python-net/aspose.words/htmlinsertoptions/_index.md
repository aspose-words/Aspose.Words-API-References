---
title: HtmlInsertOptions enumeration
linktitle: HtmlInsertOptions enumeration
articleTitle: HtmlInsertOptions enumeration
second_title: Aspose.Words for Python
description: "aspose.words.HtmlInsertOptions enumeration. Specifies options for the [DocumentBuilder.insert_html()](../documentbuilder/insert_html/#str_htmlinsertoptions) method."
type: docs
weight: 480
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
html = "<html><div style='border:dotted'><div style='border:solid'><p>paragraph 1</p><p>paragraph 2</p></div></div></html>"
# Set the new mode of import HTML block-level elements.
insert_options = aw.HtmlInsertOptions.PRESERVE_BLOCKS
builder = aw.DocumentBuilder()
builder.insert_html(html, insert_options)
builder.document.save(ARTIFACTS_DIR + "DocumentBuilder.PreserveBlocks.docx")
```

### See Also

* module [aspose.words](../)

