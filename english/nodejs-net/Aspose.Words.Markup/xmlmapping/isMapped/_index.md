---
title: XmlMapping.isMapped property
linktitle: isMapped property
articleTitle: isMapped property
second_title: Aspose.Words for NodeJs
description: "XmlMapping.isMapped property. Returns ``True`` if the parent structured document tag is successfully mapped to XML data."
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Markup/xmlmapping/isMapped/
---

## XmlMapping.isMapped property

Returns ``True`` if the parent structured document tag is successfully mapped to XML data.



```js
get isMapped(): boolean
```

### Examples

Shows how to set XML mappings for custom XML parts.

```js
let doc = new aw.Document();

// Construct an XML part that contains text and add it to the document's CustomXmlPart collection.
let xmlPartId = `{${Guid.newGuid().toString()}}`;
let xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
let xmlPart = doc.customXmlParts.add(xmlPartId, xmlPartContent);

expect(Buffer.from(xmlPart.data).toString("utf8")).toEqual("<root><text>Text element #1</text><text>Text element #2</text></root>");

// Create a structured document tag that will display the contents of our CustomXmlPart.
let tag = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.PlainText, aw.Markup.MarkupLevel.Block);

// Set a mapping for our structured document tag. This mapping will instruct
// our structured document tag to display a portion of the XML part's text contents that the XPath points to.
// In this case, it will be contents of the the second "<text>" element of the first "<root>" element: "Text element #2".
tag.xmlMapping.setMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

expect(tag.xmlMapping.isMapped).toEqual(true);
expect(tag.xmlMapping.customXmlPart).toEqual(xmlPart);
expect(tag.xmlMapping.xpath).toEqual("/root[1]/text[2]");
expect(tag.xmlMapping.prefixMappings).toEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'");

// Add the structured document tag to the document to display the content from our custom part.
doc.firstSection.body.appendChild(tag);
doc.save(base.artifactsDir + "StructuredDocumentTag.xmlMapping.docx");
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [XmlMapping](../)

