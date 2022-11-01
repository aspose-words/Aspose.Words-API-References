---
title: building_block_gallery property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies type of building block for this SDT"
type: docs
weight: 40
url: /python-net/aspose.words.markup/structureddocumenttag/building_block_gallery/
---

## StructuredDocumentTag.building_block_gallery property

Specifies type of building block for this **SDT**.
Can not be ``None``.


Accessing this property will only work for [SdtType.BUILDING_BLOCK_GALLERY](../../sdttype/#BUILDING_BLOCK_GALLERY) and
[SdtType.DOC_PART_OBJ](../../sdttype/#DOC_PART_OBJ) SDT types. It is read-only for **SDT** of the document part type.


For all other SDT types exception will occur.




### Examples

Shows how to insert a structured document tag as a building block, and set its category and gallery.

```python
doc = aw.Document()

building_block_sdt = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.BUILDING_BLOCK_GALLERY, aw.markup.MarkupLevel.BLOCK)
building_block_sdt.building_block_category = "Built-in"
building_block_sdt.building_block_gallery = "Table of Contents"

doc.first_section.body.append_child(building_block_sdt)

doc.save(ARTIFACTS_DIR + "StructuredDocumentTag.BuildingBlockCategories.docx")
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

