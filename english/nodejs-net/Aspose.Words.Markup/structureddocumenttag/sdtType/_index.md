---
title: StructuredDocumentTag.sdtType property
linktitle: sdtType property
articleTitle: sdtType property
second_title: Aspose.Words for Node.js
description: "StructuredDocumentTag.sdtType property. Gets type of this Structured document tag."
type: docs
weight: 250
url: /nodejs-net/aspose.words.markup/structureddocumenttag/sdtType/
---

## StructuredDocumentTag.sdtType property

Gets type of this **Structured document tag**.



```js
get sdtType(): Aspose.Words.Markup.SdtType
```

### Examples

Shows how to get the type of a structured document tag.

```js
let doc = new aw.Document(base.myDir + "Structured document tags.docx");

var tags = doc.getChildNodes(aw.NodeType.StructuredDocumentTag, true);

expect(tags.at(0).asStructuredDocumentTag().sdtType).toEqual(aw.Markup.SdtType.RepeatingSection);
expect(tags.at(1).asStructuredDocumentTag().sdtType).toEqual(aw.Markup.SdtType.RepeatingSectionItem);
expect(tags.at(2).asStructuredDocumentTag().sdtType).toEqual(aw.Markup.SdtType.RichText);
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [StructuredDocumentTag](../)

