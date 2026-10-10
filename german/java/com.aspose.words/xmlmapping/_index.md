---
title: "XmlMapping"
linktitle: "XmlMapping"
second_title: "Aspose.Words für Java"
description: "Gibt die Informationen an, die verwendet werden, um eine Zuordnung zwischen dem übergeordneten strukturierten Dokument-Tag und einem XML-Element, das in einem benutzerdefinierten XML-Datenpart im Dokument gespeichert ist, in Java herzustellen."
type: docs
weight: 748
url: /de/java/com.aspose.words/xmlmapping/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class XmlMapping implements Cloneable
```

Gibt die Informationen an, die verwendet werden, um eine Zuordnung zwischen dem übergeordneten strukturierten Dokument-Tag und einem XML-Element, das in einem benutzerdefinierten XML-Datenpart im Dokument gespeichert ist, herzustellen.

Weitere Informationen finden Sie im Dokumentationsartikel [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Examples:** 

Zeigt, wie XML-Zuordnungen für benutzerdefinierte XML-Teile festgelegt werden.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [delete()](#delete) | Löscht die Zuordnung des übergeordneten strukturierten Dokuments zu XML-Daten. |
| [getCustomXmlPart()](#getCustomXmlPart) | Gibt den benutzerdefinierten XML-Datenpart zurück, dem das übergeordnete strukturierte Dokument-Tag zugeordnet ist. |
| [getPrefixMappings()](#getPrefixMappings) | Gibt XML-Namespace-Präfixzuordnungen zurück, um die [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath) zu evaluieren. |
| [getStoreItemId()](#getStoreItemId) | Gibt den benutzerdefinierten XML-Datenidentifikator für den benutzerdefinierten XML-Datenpart an, der verwendet werden soll, um den [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath)-Ausdruck zu evaluieren. |
| [getXPath()](#getXPath) | Gibt den XPath-Ausdruck zurück, der ausgewertet wird, um den benutzerdefinierten XML-Knoten zu finden, der dem übergeordneten strukturierten Dokument-Tag zugeordnet ist. |
| [isMapped()](#isMapped) | Gibt  true  zurück, wenn das übergeordnete strukturierte Dokument-Tag erfolgreich zu XML-Daten zugeordnet ist. |
| [setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping)](#setMapping-com.aspose.words.CustomXmlPart-java.lang.String-java.lang.String) | Legt eine Zuordnung zwischen dem übergeordneten strukturierten Dokument-Tag und einem XML-Knoten eines benutzerdefinierten XML-Datenparts fest. |
### delete() {#delete}
```
public void delete()
```


Löscht die Zuordnung des übergeordneten strukturierten Dokuments zu XML-Daten.

 **Examples:** 

Zeigt, wie XML-Zuordnungen für benutzerdefinierte XML-Teile festgelegt werden.

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


Gibt den benutzerdefinierten XML-Datenpart zurück, dem das übergeordnete strukturierte Dokument-Tag zugeordnet ist.

 **Examples:** 

Zeigt, wie XML-Zuordnungen für benutzerdefinierte XML-Teile festgelegt werden.

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


Gibt XML-Namespace-Präfixzuordnungen zurück, um die [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath) zu evaluieren.

 **Remarks:** 

Gibt die Menge der Präfixzuordnungen an, die verwendet werden sollen, um den XPath-Ausdruck zu interpretieren, wenn der XPath-Ausdruck gegen die benutzerdefinierten XML-Datenparts im Dokument ausgewertet wird.

 **Examples:** 

Zeigt, wie XML-Zuordnungen für benutzerdefinierte XML-Teile festgelegt werden.

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
java.lang.String - XML-Namespace-Präfixzuordnungen zur Auswertung von [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath).
### getStoreItemId() {#getStoreItemId}
```
public String getStoreItemId()
```


Gibt den benutzerdefinierten XML-Datenidentifikator für den benutzerdefinierten XML-Datenpart an, der verwendet werden soll, um den [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath)-Ausdruck zu evaluieren.

 **Examples:** 

Zeigt, wie man den benutzerdefinierten XML-Datenbezeichner eines XML-Parts erhält.

```

 Document doc = new Document(getMyDir() + "Custom XML part in structured document tag.docx");

 // Structured document tags have IDs in the form of GUIDs.
 StructuredDocumentTag tag = (StructuredDocumentTag) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 0, true);

 Assert.assertEquals("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.getXmlMapping().getStoreItemId());
 
```

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getXPath() {#getXPath}
```
public String getXPath()
```


Gibt den XPath-Ausdruck zurück, der ausgewertet wird, um den benutzerdefinierten XML-Knoten zu finden, der dem übergeordneten strukturierten Dokument-Tag zugeordnet ist.

 **Examples:** 

Zeigt, wie XML-Zuordnungen für benutzerdefinierte XML-Teile festgelegt werden.

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
java.lang.String - Der XPath-Ausdruck, der ausgewertet wird, um den benutzerdefinierten XML-Knoten zu finden, der dem übergeordneten strukturierten Dokument-Tag zugeordnet ist.
### isMapped() {#isMapped}
```
public boolean isMapped()
```


Gibt  true  zurück, wenn das übergeordnete strukturierte Dokument-Tag erfolgreich zu XML-Daten zugeordnet ist.

 **Examples:** 

Zeigt, wie XML-Zuordnungen für benutzerdefinierte XML-Teile festgelegt werden.

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
boolean -  true  wenn der übergeordnete strukturierte Dokument-Tag erfolgreich auf XML-Daten abgebildet ist.
### setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping) {#setMapping-com.aspose.words.CustomXmlPart-java.lang.String-java.lang.String}
```
public boolean setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping)
```


Legt eine Zuordnung zwischen dem übergeordneten strukturierten Dokument-Tag und einem XML-Knoten eines benutzerdefinierten XML-Datenparts fest.

 **Examples:** 

Zeigt, wie man ein strukturiertes Dokumenten‑Tag mit benutzerdefinierten XML‑Daten erstellt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| customXmlPart | [CustomXmlPart](../../com.aspose.words/customxmlpart/) | Ein benutzerdefinierter XML-Datenpart, dem zugeordnet werden soll. |
| xPath | java.lang.String | Ein XPath-Ausdruck, um den XML-Knoten zu finden. |
| prefixMapping | java.lang.String | XML-Namespace-Präfixzuordnungen zur Auswertung des XPath. |

**Returns:**
boolean - Ein Flag, das angibt, ob der übergeordnete strukturierte Dokument-Tag erfolgreich auf den XML-Knoten abgebildet ist.
