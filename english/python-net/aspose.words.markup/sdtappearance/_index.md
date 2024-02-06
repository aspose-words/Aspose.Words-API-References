---
title: SdtAppearance enumeration
linktitle: SdtAppearance enumeration
articleTitle: SdtAppearance enumeration
second_title: Aspose.Words for Python
description: "aspose.words.markup.SdtAppearance enumeration. Specifies the appearance of a structured document tag."
type: docs
weight: 100
url: /python-net/aspose.words.markup/sdtappearance/
---

## SdtAppearance enumeration

Specifies the appearance of a structured document tag.


### Members

| Name | Description |
| --- | --- |
| BOUNDING_BOX | Represents a structured document tag shown as a shaded rectangle or bounding box. |
| TAGS | Represents a structured document tag shown as start and end markers. |
| HIDDEN | Represents a structured document tag that is not shown. |
| DEFAULT | Defaults to [SdtAppearance.BOUNDING_BOX](./#BOUNDING_BOX). |

### Examples

Shows how to show tag around content.

```python
doc = aw.Document(file_name=MY_DIR + "Multi-section structured document tags.docx")
tag = doc.get_child(aw.NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0,
                    True).as_structured_document_tag_range_start()

if tag.appearance == aw.markup.SdtAppearance.HIDDEN:
    tag.appearance = aw.markup.SdtAppearance.TAGS
```

### See Also

* module [aspose.words.markup](../)

