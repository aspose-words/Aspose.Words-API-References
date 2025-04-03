---
title: XmlMapping class
linktitle: XmlMapping class
articleTitle: XmlMapping class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Markup.XmlMapping class. Specifies the information that is used to establish a mapping between the parent structured document tag and an XML element stored within a custom XML data part in the document"
type: docs
weight: 210
url: /nodejs-net/Aspose.Words.Markup/xmlmapping/
---

## XmlMapping class

Specifies the information that is used to establish a mapping between the parent
structured document tag and an XML element stored within a custom XML data part in the document.
To learn more, visit the [Structured Document Tags or Content Control](https://docs.aspose.com/words/nodejs-net/working-with-content-control-sdt/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [customXmlPart](./customXmlPart/) | Returns the custom XML data part to which the parent structured document tag is mapped. |
| [isMapped](./isMapped/) | Returns ``true`` if the parent structured document tag is successfully mapped to XML data. |
| [prefixMappings](./prefixMappings/) | Returns XML namespace prefix mappings to evaluate the [XmlMapping.xpath](./xpath/). |
| [storeItemId](./storeItemId/) | Specifies the custom XML data identifier for the custom XML data part which shall be used to evaluate the [XmlMapping.xpath](./xpath/) expression. |
| [xpath](./xpath/) | Returns the XPath expression, which is evaluated to find the custom XML node that is mapped to the parent structured document tag. |

### Methods

| Name | Description |
| --- | --- |
|[ delete()](./delete/#default) | Deletes mapping of the parent structured document to XML data. |
|[ setMapping(customXmlPart, xPath, prefixMapping)](./setMapping/#customxmlpart_string_string) | Sets a mapping between the parent structured document tag and an XML node of a custom XML data part. |

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

* module [Aspose.Words.Markup](../)

