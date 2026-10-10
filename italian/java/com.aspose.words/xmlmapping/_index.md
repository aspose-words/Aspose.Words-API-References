---
title: "XmlMapping"
linktitle: "XmlMapping"
second_title: "Aspose.Words per Java"
description: "Specifica le informazioni utilizzate per stabilire una mappatura tra il tag di documento strutturato padre e un elemento XML memorizzato all'interno di una parte di dati XML personalizzata nel documento in Java."
type: docs
weight: 748
url: /it/java/com.aspose.words/xmlmapping/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class XmlMapping implements Cloneable
```

Specifica le informazioni utilizzate per stabilire una mappatura tra il tag del documento strutturato padre e un elemento XML memorizzato all'interno di una parte dati XML personalizzata nel documento.

Per saperne di più, visita l'articolo di documentazione [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Examples:** 

Mostra come impostare le mappature XML per le parti XML personalizzate.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [delete()](#delete) | Elimina la mappatura del documento strutturato padre ai dati XML. |
| [getCustomXmlPart()](#getCustomXmlPart) | Restituisce la parte di dati XML personalizzata a cui è mappato il tag del documento strutturato padre. |
| [getPrefixMappings()](#getPrefixMappings) | Restituisce le mappature dei prefissi dello spazio dei nomi XML per valutare il [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath). |
| [getStoreItemId()](#getStoreItemId) | Specifica l'identificatore dei dati XML personalizzati per la parte di dati XML personalizzata che deve essere utilizzata per valutare l'espressione [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath). |
| [getXPath()](#getXPath) | Restituisce l'espressione XPath, che viene valutata per trovare il nodo XML personalizzato mappato al tag del documento strutturato padre. |
| [isMapped()](#isMapped) | Restituisce  true  se il tag del documento strutturato padre è mappato con successo ai dati XML. |
| [setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping)](#setMapping-com.aspose.words.CustomXmlPart-java.lang.String-java.lang.String) | Imposta una mappatura tra il tag del documento strutturato padre e un nodo XML di una parte di dati XML personalizzata. |
### delete() {#delete}
```
public void delete()
```


Elimina la mappatura del documento strutturato padre ai dati XML.

 **Examples:** 

Mostra come impostare le mappature XML per le parti XML personalizzate.

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


Restituisce la parte di dati XML personalizzata a cui è mappato il tag del documento strutturato padre.

 **Examples:** 

Mostra come impostare le mappature XML per le parti XML personalizzate.

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


Restituisce le mappature dei prefissi dello spazio dei nomi XML per valutare il [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath).

 **Remarks:** 

Specifica l'insieme delle mappature dei prefissi, che devono essere utilizzate per interpretare l'espressione XPath quando l'espressione XPath viene valutata rispetto alle parti di dati XML personalizzate nel documento.

 **Examples:** 

Mostra come impostare le mappature XML per le parti XML personalizzate.

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
java.lang.String - Mappature dei prefissi dello spazio dei nomi XML per valutare il [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath).
### getStoreItemId() {#getStoreItemId}
```
public String getStoreItemId()
```


Specifica l'identificatore dei dati XML personalizzati per la parte di dati XML personalizzata che deve essere utilizzata per valutare l'espressione [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath).

 **Examples:** 

Mostra come ottenere l'identificatore dei dati XML personalizzati di una parte XML.

```

 Document doc = new Document(getMyDir() + "Custom XML part in structured document tag.docx");

 // Structured document tags have IDs in the form of GUIDs.
 StructuredDocumentTag tag = (StructuredDocumentTag) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 0, true);

 Assert.assertEquals("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.getXmlMapping().getStoreItemId());
 
```

**Returns:**
java.lang.String - Il valore java.lang.String corrispondente.
### getXPath() {#getXPath}
```
public String getXPath()
```


Restituisce l'espressione XPath, che viene valutata per trovare il nodo XML personalizzato mappato al tag del documento strutturato padre.

 **Examples:** 

Mostra come impostare le mappature XML per le parti XML personalizzate.

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
java.lang.String - L'espressione XPath, che viene valutata per trovare il nodo XML personalizzato mappato al tag del documento strutturato padre.
### isMapped() {#isMapped}
```
public boolean isMapped()
```


Restituisce  true  se il tag del documento strutturato padre è mappato con successo ai dati XML.

 **Examples:** 

Mostra come impostare le mappature XML per le parti XML personalizzate.

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
boolean -  true  se il tag del documento strutturato padre è mappato con successo ai dati XML.
### setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping) {#setMapping-com.aspose.words.CustomXmlPart-java.lang.String-java.lang.String}
```
public boolean setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping)
```


Imposta una mappatura tra il tag del documento strutturato padre e un nodo XML di una parte di dati XML personalizzata.

 **Examples:** 

Mostra come creare un tag di documento strutturato con dati XML personalizzati.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| customXmlPart | [CustomXmlPart](../../com.aspose.words/customxmlpart/) | Una parte dati XML personalizzata a cui mappare. |
| xPath | java.lang.String | Un'espressione XPath per trovare il nodo XML. |
| prefixMapping | java.lang.String | Mappature dei prefissi degli spazi dei nomi XML per valutare l'XPath. |

**Returns:**
boolean - Un flag che indica se il tag del documento strutturato padre è stato mappato correttamente al nodo XML.
