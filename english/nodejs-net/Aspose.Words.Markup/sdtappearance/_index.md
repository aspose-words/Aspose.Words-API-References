---
title: SdtAppearance enumeration
linktitle: SdtAppearance enumeration
articleTitle: SdtAppearance enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Markup.SdtAppearance enumeration. Specifies the appearance of a structured document tag."
type: docs
weight: 100
url: /nodejs-net/Aspose.Words.Markup/sdtappearance/
---

## SdtAppearance enumeration

Specifies the appearance of a structured document tag.


### Members

| Name | Description |
| --- | --- |
| BoundingBox | Represents a structured document tag shown as a shaded rectangle or bounding box. |
| Tags | Represents a structured document tag shown as start and end markers. |
| Hidden | Represents a structured document tag that is not shown. |
| Default | Defaults to [SdtAppearance.BoundingBox](./#BoundingBox). |

### Examples

Shows how to show tag around content.

```js
let doc = new aw.Document(base.myDir + "Multi-section structured document tags.docx");
let tag = doc.getChild(aw.NodeType.StructuredDocumentTagRangeStart, 0, true).asStructuredDocumentTagRangeStart();

if (tag.appearance == aw.Markup.SdtAppearance.Hidden)
  tag.appearance = aw.Markup.SdtAppearance.Tags;
```

### See Also

* module [Aspose.Words.Markup](../)

