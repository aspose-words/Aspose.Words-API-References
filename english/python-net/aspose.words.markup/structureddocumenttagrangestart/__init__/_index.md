---
title: StructuredDocumentTagRangeStart constructor
linktitle: StructuredDocumentTagRangeStart constructor
articleTitle: StructuredDocumentTagRangeStart constructor
second_title: Aspose.Words for Python
description: "StructuredDocumentTagRangeStart constructor. Initializes a new instance of the Structured document tag range start class."
type: docs
weight: 10
url: /python-net/aspose.words.markup/structureddocumenttagrangestart/__init__/
---

## StructuredDocumentTagRangeStart(doc, type) {#documentbase_sdttype}

Initializes a new instance of the **Structured document tag range start** class.



```python
def __init__(self, doc: aspose.words.DocumentBase, type: aspose.words.markup.SdtType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../../aspose.words/documentbase/) | The owner document. |
| type | [SdtType](../../sdttype/) | Type of SDT node. |

### Remarks

The following types of SDT can be created:


* [SdtType.CHECKBOX](../../sdttype/#CHECKBOX)
  
  
* [SdtType.DROP_DOWN_LIST](../../sdttype/#DROP_DOWN_LIST)
  
  
* [SdtType.COMBO_BOX](../../sdttype/#COMBO_BOX)
  
  
* [SdtType.DATE](../../sdttype/#DATE)
  
  
* [SdtType.BUILDING_BLOCK_GALLERY](../../sdttype/#BUILDING_BLOCK_GALLERY)
  
  
* [SdtType.GROUP](../../sdttype/#GROUP)
  
  
* [SdtType.PICTURE](../../sdttype/#PICTURE)
  
  
* [SdtType.RICH_TEXT](../../sdttype/#RICH_TEXT)
  
  
* [SdtType.PLAIN_TEXT](../../sdttype/#PLAIN_TEXT)
  
  



### Examples

Shows how to create/remove structured document tag and its content (InsertStructuredDocumentTagRanges).

```python
def insert_structured_document_tag_ranges(self, doc):
    range_start = aw.markup.StructuredDocumentTagRangeStart(doc, aw.markup.SdtType.PLAIN_TEXT)
    range_end = aw.markup.StructuredDocumentTagRangeEnd(doc, range_start.id)
    doc.first_section.body.insert_before(range_start, doc.first_section.body.first_paragraph)
    doc.last_section.body.insert_after(range_end, doc.first_section.body.first_paragraph)
    return range_start
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTagRangeStart](../)

