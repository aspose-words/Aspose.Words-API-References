---
title: CustomXmlPart.dataChecksum property
linktitle: dataChecksum property
articleTitle: dataChecksum property
second_title: Aspose.Words for Node.js
description: "CustomXmlPart.dataChecksum property. Specifies a cyclic redundancy check (CRC) checksum of the [CustomXmlPart.data](../data/) content."
type: docs
weight: 30
url: /nodejs-net/aspose.words.markup/customxmlpart/dataChecksum/
---

## CustomXmlPart.dataChecksum property

Specifies a cyclic redundancy check (CRC) checksum of the [CustomXmlPart.data](../data/) content.



```js
get dataChecksum(): number
```

### Examples

Shows how the checksum is calculated in a runtime.

```js
let doc = new aw.Document();

let richText = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.RichText, aw.Markup.MarkupLevel.Block);
doc.firstSection.body.appendChild(richText);

// The checksum is read-only and computed using the data of the corresponding custom XML data part.
richText.xmlMapping.setMapping(doc.customXmlParts.add(Guid.newGuid().toString(),
  "<root><text>ContentControl</text></root>"), "/root/text", "");

let checksum = richText.xmlMapping.customXmlPart.dataChecksum;
console.log(checksum);

richText.xmlMapping.setMapping(doc.customXmlParts.add(Guid.newGuid().toString(),
  "<root><text>Updated ContentControl</text></root>"), "/root/text", "");

let updatedChecksum = richText.xmlMapping.customXmlPart.dataChecksum;
console.log(updatedChecksum);

// We changed the XmlPart of the tag, and the checksum was updated at runtime.
expect(updatedChecksum).not.toEqual(checksum);
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [CustomXmlPart](../)

