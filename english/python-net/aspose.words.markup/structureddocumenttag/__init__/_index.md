---
title: StructuredDocumentTag constructor
linktitle: StructuredDocumentTag constructor
articleTitle: StructuredDocumentTag constructor
second_title: Aspose.Words for Python
description: "StructuredDocumentTag constructor. Initializes a new instance of the Structured document tag class."
type: docs
weight: 10
url: /python-net/aspose.words.markup/structureddocumenttag/__init__/
---

## StructuredDocumentTag(doc, type, level) {#documentbase_sdttype_markuplevel}

Initializes a new instance of the **Structured document tag** class.



```python
def __init__(self, doc: aspose.words.DocumentBase, type: aspose.words.markup.SdtType, level: aspose.words.markup.MarkupLevel):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../../aspose.words/documentbase/) | The owner document. |
| type | [SdtType](../../sdttype/) | Type of SDT node. |
| level | [MarkupLevel](../../markuplevel/) | Level of SDT node within the document. |

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

Show how to create a structured document tag in the form of a check box.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
sdt_check_box = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.CHECKBOX, aw.markup.MarkupLevel.INLINE)
sdt_check_box.checked = True
# We can set the symbols used to represent the checked/unchecked state of a checkbox content control.
sdt_check_box.set_checked_symbol(169, 'Times New Roman')
sdt_check_box.set_unchecked_symbol(174, 'Times New Roman')
builder.insert_node(sdt_check_box)
doc.save(ARTIFACTS_DIR + 'StructuredDocumentTag.check_box.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

