---
title: StructuredDocumentTagRangeStart.xmlMapping property
linktitle: xmlMapping property
articleTitle: xmlMapping property
second_title: Aspose.Words for NodeJs
description: "StructuredDocumentTagRangeStart.xmlMapping property. Gets an object that represents the mapping of this structured document tag range to XML data in a custom XML part of the current document."
type: docs
weight: 190
url: /nodejs-net/aspose.words.markup/structureddocumenttagrangestart/xmlMapping/
---

## StructuredDocumentTagRangeStart.xmlMapping property

Gets an object that represents the mapping of this structured document tag range to XML data
in a custom XML part of the current document.


```js
get xmlMapping(): Aspose.Words.Markup.XmlMapping
```

### Remarks

You can use the [XmlMapping.setMapping()](../../xmlmapping/setMapping/#customxmlpart_string_string) method of this
object to map a structured document tag range to XML data.



### Examples

Shows how to set XML mappings for the range start of a structured document tag.

```js
let doc = new aw.Document(base.myDir + "Multi-section structured document tags.docx");

// Construct an XML part that contains text and add it to the document's CustomXmlPart collection.
let xmlPartId = `{${Guid.newGuid().toString()}}`;
let xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
let xmlPart = doc.customXmlParts.add(xmlPartId, xmlPartContent);

expect(Buffer.from(xmlPart.data).toString("utf8")).toEqual("<root><text>Text element #1</text><text>Text element #2</text></root>");

// Create a structured document tag that will display the contents of our CustomXmlPart in the document.
let sdtRangeStart = doc.getChild(aw.NodeType.StructuredDocumentTagRangeStart, 0, true).asStructuredDocumentTagRangeStart();

// If we set a mapping for our structured document tag,
// it will only display a portion of the CustomXmlPart that the XPath points to.
// This XPath will point to the contents second "<text>" element of the first "<root>" element of our CustomXmlPart.
sdtRangeStart.xmlMapping.setMapping(xmlPart, "/root[1]/text[2]", null);

doc.save(base.artifactsDir + "StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [StructuredDocumentTagRangeStart](../)

