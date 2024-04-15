---
title: XmlMapping
linktitle: XmlMapping
second_title: Aspose.Words for Java
description: Specifies the information that is used to establish a mapping between the parent structured document tag and an XML element stored within a custom XML data part in the document in Java.
type: docs
weight: 674
url: /java/com.aspose.words/xmlmapping/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class XmlMapping implements Cloneable
```

Specifies the information that is used to establish a mapping between the parent structured document tag and an XML element stored within a custom XML data part in the document.

To learn more, visit the [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control] documentation article.

 **Examples:** 

Shows how to set XML mappings for custom XML parts.

```

 Document doc = new Document();

 // Construct an XML part that contains text and add it to the document's CustomXmlPart collection.
 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Text element #1Text element #2";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Create a structured document tag that will display the contents of our CustomXmlPart.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.BLOCK);

 // Set a mapping for our structured document tag. This mapping will instruct
 // our structured document tag to display a portion of the XML part's text contents that the XPath points to.
 // In this case, it will be contents of the the second "" element of the first "" element: "Text element #2".
 tag.getXmlMapping().setMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

 Assert.assertTrue(tag.getXmlMapping().isMapped());
 Assert.assertEquals(tag.getXmlMapping().getCustomXmlPart(), xmlPart);
 Assert.assertEquals(tag.getXmlMapping().getXPath(), "/root[1]/text[2]");
 Assert.assertEquals(tag.getXmlMapping().getPrefixMappings(), "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

 // Add the structured document tag to the document to display the content from our custom part.
 doc.getFirstSection().getBody().appendChild(tag);
 doc.save(getArtifactsDir() + "StructuredDocumentTag.XmlMapping.docx");
 
```


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## Methods

| Method | Description |
| --- | --- |
| [delete()](#delete) | Deletes mapping of the parent structured document to XML data. |
| [getCustomXmlPart()](#getCustomXmlPart) | Returns the custom XML data part to which the parent structured document tag is mapped. |
| [getPrefixMappings()](#getPrefixMappings) | Returns XML namespace prefix mappings to evaluate the [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath). |
| [getStoreItemId()](#getStoreItemId) | Specifies the custom XML data identifier for the custom XML data part which shall be used to evaluate the [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath) expression. |
| [getXPath()](#getXPath) | Returns the XPath expression, which is evaluated to find the custom XML node that is mapped to the parent structured document tag. |
| [isMapped()](#isMapped) | Returns  true  if the parent structured document tag is successfully mapped to XML data. |
| [setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping)](#setMapping-com.aspose.words.CustomXmlPart-java.lang.String-java.lang.String) | Sets a mapping between the parent structured document tag and an XML node of a custom XML data part. |
### delete() {#delete}
```
public void delete()
```


Deletes mapping of the parent structured document to XML data.

 **Examples:** 

Shows how to set XML mappings for custom XML parts.

```

 Document doc = new Document();

 // Construct an XML part that contains text and add it to the document's CustomXmlPart collection.
 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Text element #1Text element #2";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Create a structured document tag that will display the contents of our CustomXmlPart.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.BLOCK);

 // Set a mapping for our structured document tag. This mapping will instruct
 // our structured document tag to display a portion of the XML part's text contents that the XPath points to.
 // In this case, it will be contents of the the second "" element of the first "" element: "Text element #2".
 tag.getXmlMapping().setMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

 Assert.assertTrue(tag.getXmlMapping().isMapped());
 Assert.assertEquals(tag.getXmlMapping().getCustomXmlPart(), xmlPart);
 Assert.assertEquals(tag.getXmlMapping().getXPath(), "/root[1]/text[2]");
 Assert.assertEquals(tag.getXmlMapping().getPrefixMappings(), "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

 // Add the structured document tag to the document to display the content from our custom part.
 doc.getFirstSection().getBody().appendChild(tag);
 doc.save(getArtifactsDir() + "StructuredDocumentTag.XmlMapping.docx");
 
```

### getCustomXmlPart() {#getCustomXmlPart}
```
public CustomXmlPart getCustomXmlPart()
```


Returns the custom XML data part to which the parent structured document tag is mapped.

 **Examples:** 

Shows how to set XML mappings for custom XML parts.

```

 Document doc = new Document();

 // Construct an XML part that contains text and add it to the document's CustomXmlPart collection.
 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Text element #1Text element #2";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Create a structured document tag that will display the contents of our CustomXmlPart.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.BLOCK);

 // Set a mapping for our structured document tag. This mapping will instruct
 // our structured document tag to display a portion of the XML part's text contents that the XPath points to.
 // In this case, it will be contents of the the second "" element of the first "" element: "Text element #2".
 tag.getXmlMapping().setMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

 Assert.assertTrue(tag.getXmlMapping().isMapped());
 Assert.assertEquals(tag.getXmlMapping().getCustomXmlPart(), xmlPart);
 Assert.assertEquals(tag.getXmlMapping().getXPath(), "/root[1]/text[2]");
 Assert.assertEquals(tag.getXmlMapping().getPrefixMappings(), "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

 // Add the structured document tag to the document to display the content from our custom part.
 doc.getFirstSection().getBody().appendChild(tag);
 doc.save(getArtifactsDir() + "StructuredDocumentTag.XmlMapping.docx");
 
```

**Returns:**
[CustomXmlPart](../../com.aspose.words/customxmlpart/) - The custom XML data part to which the parent structured document tag is mapped.
### getPrefixMappings() {#getPrefixMappings}
```
public String getPrefixMappings()
```


Returns XML namespace prefix mappings to evaluate the [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath).

 **Remarks:** 

Specifies the set of prefix mappings, which shall be used to interpret the XPath expression when the XPath expression is evaluated against the custom XML data parts in the document.

 **Examples:** 

Shows how to set XML mappings for custom XML parts.

```

 Document doc = new Document();

 // Construct an XML part that contains text and add it to the document's CustomXmlPart collection.
 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Text element #1Text element #2";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Create a structured document tag that will display the contents of our CustomXmlPart.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.BLOCK);

 // Set a mapping for our structured document tag. This mapping will instruct
 // our structured document tag to display a portion of the XML part's text contents that the XPath points to.
 // In this case, it will be contents of the the second "" element of the first "" element: "Text element #2".
 tag.getXmlMapping().setMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

 Assert.assertTrue(tag.getXmlMapping().isMapped());
 Assert.assertEquals(tag.getXmlMapping().getCustomXmlPart(), xmlPart);
 Assert.assertEquals(tag.getXmlMapping().getXPath(), "/root[1]/text[2]");
 Assert.assertEquals(tag.getXmlMapping().getPrefixMappings(), "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

 // Add the structured document tag to the document to display the content from our custom part.
 doc.getFirstSection().getBody().appendChild(tag);
 doc.save(getArtifactsDir() + "StructuredDocumentTag.XmlMapping.docx");
 
```

**Returns:**
java.lang.String - XML namespace prefix mappings to evaluate the [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath).
### getStoreItemId() {#getStoreItemId}
```
public String getStoreItemId()
```


Specifies the custom XML data identifier for the custom XML data part which shall be used to evaluate the [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath) expression.

 **Examples:** 

Shows how to get the custom XML data identifier of an XML part.

```

 Document doc = new Document(getMyDir() + "Custom XML part in structured document tag.docx");

 // Structured document tags have IDs in the form of GUIDs.
 StructuredDocumentTag tag = (StructuredDocumentTag) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 0, true);

 Assert.assertEquals("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.getXmlMapping().getStoreItemId());
 
```

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getXPath() {#getXPath}
```
public String getXPath()
```


Returns the XPath expression, which is evaluated to find the custom XML node that is mapped to the parent structured document tag.

 **Examples:** 

Shows how to set XML mappings for custom XML parts.

```

 Document doc = new Document();

 // Construct an XML part that contains text and add it to the document's CustomXmlPart collection.
 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Text element #1Text element #2";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Create a structured document tag that will display the contents of our CustomXmlPart.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.BLOCK);

 // Set a mapping for our structured document tag. This mapping will instruct
 // our structured document tag to display a portion of the XML part's text contents that the XPath points to.
 // In this case, it will be contents of the the second "" element of the first "" element: "Text element #2".
 tag.getXmlMapping().setMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

 Assert.assertTrue(tag.getXmlMapping().isMapped());
 Assert.assertEquals(tag.getXmlMapping().getCustomXmlPart(), xmlPart);
 Assert.assertEquals(tag.getXmlMapping().getXPath(), "/root[1]/text[2]");
 Assert.assertEquals(tag.getXmlMapping().getPrefixMappings(), "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

 // Add the structured document tag to the document to display the content from our custom part.
 doc.getFirstSection().getBody().appendChild(tag);
 doc.save(getArtifactsDir() + "StructuredDocumentTag.XmlMapping.docx");
 
```

**Returns:**
java.lang.String - The XPath expression, which is evaluated to find the custom XML node that is mapped to the parent structured document tag.
### isMapped() {#isMapped}
```
public boolean isMapped()
```


Returns  true  if the parent structured document tag is successfully mapped to XML data.

 **Examples:** 

Shows how to set XML mappings for custom XML parts.

```

 Document doc = new Document();

 // Construct an XML part that contains text and add it to the document's CustomXmlPart collection.
 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Text element #1Text element #2";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 // Create a structured document tag that will display the contents of our CustomXmlPart.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.BLOCK);

 // Set a mapping for our structured document tag. This mapping will instruct
 // our structured document tag to display a portion of the XML part's text contents that the XPath points to.
 // In this case, it will be contents of the the second "" element of the first "" element: "Text element #2".
 tag.getXmlMapping().setMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

 Assert.assertTrue(tag.getXmlMapping().isMapped());
 Assert.assertEquals(tag.getXmlMapping().getCustomXmlPart(), xmlPart);
 Assert.assertEquals(tag.getXmlMapping().getXPath(), "/root[1]/text[2]");
 Assert.assertEquals(tag.getXmlMapping().getPrefixMappings(), "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

 // Add the structured document tag to the document to display the content from our custom part.
 doc.getFirstSection().getBody().appendChild(tag);
 doc.save(getArtifactsDir() + "StructuredDocumentTag.XmlMapping.docx");
 
```

**Returns:**
boolean -  true  if the parent structured document tag is successfully mapped to XML data.
### setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping) {#setMapping-com.aspose.words.CustomXmlPart-java.lang.String-java.lang.String}
```
public boolean setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping)
```


Sets a mapping between the parent structured document tag and an XML node of a custom XML data part.

 **Examples:** 

Shows how to create a structured document tag with custom XML data.

```

 Document doc = new Document();

 // Construct an XML part that contains data and add it to the document's collection.
 // If we enable the "Developer" tab in Microsoft Word,
 // we can find elements from this collection in the "XML Mapping Pane", along with a few default elements.
 String xmlPartId = UUID.randomUUID().toString();
 String xmlPartContent = "Hello, World!";
 CustomXmlPart xmlPart = doc.getCustomXmlParts().add(xmlPartId, xmlPartContent);

 Assert.assertEquals(xmlPart.getData(), xmlPartContent.getBytes());
 Assert.assertEquals(xmlPart.getId(), xmlPartId);

 // Below are two ways to refer to XML parts.
 // 1 -  By an index in the custom XML part collection:
 Assert.assertEquals(xmlPart, doc.getCustomXmlParts().get(0));

 // 2 -  By GUID:
 Assert.assertEquals(xmlPart, doc.getCustomXmlParts().getById(xmlPartId));

 // Add an XML schema association.
 xmlPart.getSchemas().add("http://www.w3.org/2001/XMLSchema");

 // Clone a part, and then insert it into the collection.
 CustomXmlPart xmlPartClone = xmlPart.deepClone();
 xmlPartClone.setId(UUID.randomUUID().toString());
 doc.getCustomXmlParts().add(xmlPartClone);

 Assert.assertEquals(doc.getCustomXmlParts().getCount(), 2);

 // Iterate through the collection and print the contents of each part.
 Iterator enumerator = doc.getCustomXmlParts().iterator();
 int index = 0;
 while (enumerator.hasNext()) {
     CustomXmlPart customXmlPart = enumerator.next();
     System.out.println(MessageFormat.format("XML part index {0}, ID: {1}", index, customXmlPart.getId()));
     System.out.println(MessageFormat.format("\tContent: {0}", customXmlPart.getData()));
     index++;
 }

 // Use the "RemoveAt" method to remove the cloned part by index.
 doc.getCustomXmlParts().removeAt(1);

 Assert.assertEquals(doc.getCustomXmlParts().getCount(), 1);

 // Clone the XML parts collection, and then use the "Clear" method to remove all its elements at once.
 CustomXmlPartCollection customXmlParts = doc.getCustomXmlParts().deepClone();
 customXmlParts.clear();

 // Create a structured document tag that will display our part's contents and insert it into the document body.
 StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PLAIN_TEXT, MarkupLevel.BLOCK);
 tag.getXmlMapping().setMapping(xmlPart, "/root[1]/text[1]", "");

 doc.getFirstSection().getBody().appendChild(tag);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.CustomXml.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| customXmlPart | [CustomXmlPart](../../com.aspose.words/customxmlpart/) | A custom XML data part to map to. |
| xPath | java.lang.String | An XPath expression to find the XML node. |
| prefixMapping | java.lang.String | XML namespace prefix mappings to evaluate the XPath. |

**Returns:**
boolean - A flag indicating whether the parent structured document tag is successfully mapped to the XML node.
