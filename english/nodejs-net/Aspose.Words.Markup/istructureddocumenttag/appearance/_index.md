﻿---
title: IStructuredDocumentTag.appearance property
linktitle: appearance property
articleTitle: appearance property
second_title: Aspose.Words for Node.js
description: "IStructuredDocumentTag.appearance property. Gets or sets the appearance of the structured document tag."
type: docs
weight: 10
url: /nodejs-net/aspose.words.markup/istructureddocumenttag/appearance/
---

## IStructuredDocumentTag.appearance property

Gets or sets the appearance of the structured document tag.


```js
get appearance(): Aspose.Words.Markup.SdtAppearance
```

### Examples

Shows how to show tag around content.

```js
let doc = new aw.Document(base.myDir + "Multi-section structured document tags.docx");
let tag = doc.getChild(aw.NodeType.StructuredDocumentTagRangeStart, 0, true).asStructuredDocumentTagRangeStart();

if (tag.appearance == aw.Markup.SdtAppearance.Hidden)
  tag.appearance = aw.Markup.SdtAppearance.Tags;
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [IStructuredDocumentTag](../)

