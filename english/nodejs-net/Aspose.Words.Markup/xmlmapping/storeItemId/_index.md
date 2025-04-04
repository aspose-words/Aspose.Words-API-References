---
title: XmlMapping.storeItemId property
linktitle: storeItemId property
articleTitle: storeItemId property
second_title: Aspose.Words for Node.js
description: "XmlMapping.storeItemId property. Specifies the custom XML data identifier for the custom XML data part which shall be used to evaluate the [XmlMapping.xpath](../xpath/) expression."
type: docs
weight: 40
url: /nodejs-net/aspose.words.markup/xmlmapping/storeItemId/
---

## XmlMapping.storeItemId property

Specifies the custom XML data identifier for the custom XML data part which
shall be used to evaluate the [XmlMapping.xpath](../xpath/) expression.



```js
get storeItemId(): string
```

### Examples

Shows how to get the custom XML data identifier of an XML part.

```js
let doc = new aw.Document(base.myDir + "Custom XML part in structured document tag.docx");

// Structured document tags have IDs in the form of GUIDs.
let tag = doc.getChild(aw.NodeType.StructuredDocumentTag, 0, true).asStructuredDocumentTag();

expect(tag.xmlMapping.storeItemId).toEqual("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}");
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [XmlMapping](../)

