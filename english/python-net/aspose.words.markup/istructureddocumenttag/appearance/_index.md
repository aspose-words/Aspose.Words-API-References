---
title: IStructuredDocumentTag.appearance property
linktitle: appearance property
articleTitle: appearance property
second_title: Aspose.Words for Python
description: "IStructuredDocumentTag.appearance property. Gets or sets the appearance of the structured document tag."
type: docs
weight: 10
url: /python-net/aspose.words.markup/istructureddocumenttag/appearance/
---

## IStructuredDocumentTag.appearance property

Gets or sets the appearance of the structured document tag.


```python
@property
def appearance(self) -> aspose.words.markup.SdtAppearance:
    ...

@appearance.setter
def appearance(self, value: aspose.words.markup.SdtAppearance):
    ...

```

### Examples

Shows how to show tag around content.

```python
doc = aw.Document(file_name=MY_DIR + 'Multi-section structured document tags.docx')
tag = doc.get_child(aw.NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, True).as_structured_document_tag_range_start()
if tag.appearance == aw.markup.SdtAppearance.HIDDEN:
    tag.appearance = aw.markup.SdtAppearance.TAGS
```

### See Also

* module [aspose.words.markup](../../)
* class [IStructuredDocumentTag](../)

