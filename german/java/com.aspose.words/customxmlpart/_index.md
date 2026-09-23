---
title: "CustomXmlPart"
linktitle: "CustomXmlPart"
second_title: "Aspose.Words für Java"
description: "Stellt einen Custom XML Data Storage Part mit benutzerdefinierten XML‑Daten innerhalb eines Pakets in Java dar."
type: docs
weight: 143
url: /de/java/com.aspose.words/customxmlpart/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class CustomXmlPart implements Cloneable
```

Stellt einen Custom XML Data Storage Part dar (benutzerdefinierte XML‑Daten innerhalb eines Pakets).

Weitere Informationen finden Sie im Dokumentationsartikel [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Remarks:** 

Ein DOCX- oder DOC-Dokument kann einen oder mehrere Custom XML Data Storage‑Teile enthalten. Aspose.Words bewahrt sie und ermöglicht das Erstellen und Extrahieren von Custom XML Data über die Sammlung [Document.getCustomXmlParts()](../../com.aspose.words/document/\#getCustomXmlParts) / [Document.setCustomXmlParts(com.aspose.words.CustomXmlPartCollection)](../../com.aspose.words/document/\#setCustomXmlParts-com.aspose.words.CustomXmlPartCollection).

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


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/working-with-content-control-sdt/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [deepClone()](#deepClone) | Erstellt eine "deep enough" Kopie des Objekts. |
| [getData()](#getData) | Liest den XML‑Inhalt dieses Custom XML Data Storage Parts. |
| [getDataChecksum()](#getDataChecksum) | Gibt eine zyklische Redundanzprüfung (CRC)-Prüfsumme des [getData()](../../com.aspose.words/customxmlpart/\#getData) / [setData(byte[])](../../com.aspose.words/customxmlpart/\#setData-byte) Inhalts an. |
| [getId()](#getId) | Liest die Zeichenkette, die diesen benutzerdefinierten XML‑Teil innerhalb eines OOXML‑Dokuments identifiziert. |
| [getSchemas()](#getSchemas) | Gibt den Satz von XML‑Schemata an, die mit diesem benutzerdefinierten XML‑Teil verknüpft sind. |
| [setData(byte[] value)](#setData-byte) | Legt den XML‑Inhalt dieses Custom XML Data Storage Parts fest. |
| [setId(String value)](#setId-java.lang.String) | Legt die Zeichenkette fest, die diesen benutzerdefinierten XML‑Teil innerhalb eines OOXML‑Dokuments identifiziert. |
### deepClone() {#deepClone}
```
public CustomXmlPart deepClone()
```


Erstellt eine \"deep enough\" Kopie des Objekts. Dupliziert nicht die Bytes des [getData()](../../com.aspose.words/customxmlpart/\#getData) / [setData(byte[])](../../com.aspose.words/customxmlpart/\#setData-byte) Werts.

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

**Returns:**
[CustomXmlPart](../../com.aspose.words/customxmlpart/)
### getData() {#getData}
```
public byte[] getData()
```


Liest den XML‑Inhalt dieses Custom XML Data Storage Parts.

 **Remarks:** 

Der Standardwert ist ein leeres Byte‑Array. Der Wert darf nicht null sein.

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

**Returns:**
byte[] - Der XML‑Inhalt dieses Custom XML Data Storage Parts.
### getDataChecksum() {#getDataChecksum}
```
public long getDataChecksum()
```


Gibt eine zyklische Redundanzprüfung (CRC)-Prüfsumme des [getData()](../../com.aspose.words/customxmlpart/\#getData) / [setData(byte[])](../../com.aspose.words/customxmlpart/\#setData-byte) Inhalts an.

 **Examples:** 

Zeigt, wie die Prüfsumme zur Laufzeit berechnet wird.

```

 Document doc = new Document();

 StructuredDocumentTag richText = new StructuredDocumentTag(doc, SdtType.RICH_TEXT, MarkupLevel.BLOCK);
 doc.getFirstSection().getBody().appendChild(richText);

 // The checksum is read-only and computed using the data of the corresponding custom XML data part.
 richText.getXmlMapping().setMapping(doc.getCustomXmlParts().add(UUID.randomUUID().toString(),
         "ContentControl"), "/root/text", "");

 long checksum = richText.getXmlMapping().getCustomXmlPart().getDataChecksum();
 System.out.println(checksum);

 richText.getXmlMapping().setMapping(doc.getCustomXmlParts().add(UUID.randomUUID().toString(),
         "Updated ContentControl"), "/root/text", "");

 long updatedChecksum = richText.getXmlMapping().getCustomXmlPart().getDataChecksum();
 System.out.println(updatedChecksum);

 // We changed the XmlPart of the tag, and the checksum was updated at runtime.
 Assert.assertNotEquals(checksum, updatedChecksum);
 
```

**Returns:**
long - Der entsprechende long‑Wert.
### getId() {#getId}
```
public String getId()
```


Liest die Zeichenkette, die diesen benutzerdefinierten XML‑Teil innerhalb eines OOXML‑Dokuments identifiziert.

 **Remarks:** 

ISO/IEC 29500 gibt an, dass dieser Wert eine GUID ist, aber alte Versionen von Microsoft Word erlaubten hier beliebige Zeichenketten. Aspose.Words verhält sich im ECMA‑376‑Format genauso. Beachten Sie jedoch, dass Microsoft Word Online ein Dokument, das mit einem Nicht‑GUID‑Wert erstellt wurde, nicht öffnen kann. Daher wird für diese Eigenschaft bevorzugt eine GUID verwendet.

Ein gültiger Wert muss ein Bezeichner sein, der unter allen benutzerdefinierten XML‑Daten‑Teilen in diesem Dokument eindeutig ist.

Der Standardwert ist eine leere Zeichenkette. Der Wert darf nicht null sein.

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

**Returns:**
java.lang.String - Die Zeichenkette, die diesen benutzerdefinierten XML‑Teil innerhalb eines OOXML‑Dokuments identifiziert.
### getSchemas() {#getSchemas}
```
public CustomXmlSchemaCollection getSchemas()
```


Gibt den Satz von XML‑Schemata an, die mit diesem benutzerdefinierten XML‑Teil verknüpft sind.

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

**Returns:**
[CustomXmlSchemaCollection](../../com.aspose.words/customxmlschemacollection/) - The corresponding [CustomXmlSchemaCollection](../../com.aspose.words/customxmlschemacollection/) value.
### setData(byte[] value) {#setData-byte}
```
public void setData(byte[] value)
```


Legt den XML‑Inhalt dieses Custom XML Data Storage Parts fest.

 **Remarks:** 

Der Standardwert ist ein leeres Byte‑Array. Der Wert darf nicht null sein.

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
| Wert | byte[] | Der XML‑Inhalt dieses Custom XML Data Storage Parts. |

### setId(String value) {#setId-java.lang.String}
```
public void setId(String value)
```


Legt die Zeichenkette fest, die diesen benutzerdefinierten XML‑Teil innerhalb eines OOXML‑Dokuments identifiziert.

 **Remarks:** 

ISO/IEC 29500 gibt an, dass dieser Wert eine GUID ist, aber alte Versionen von Microsoft Word erlaubten hier beliebige Zeichenketten. Aspose.Words verhält sich im ECMA‑376‑Format genauso. Beachten Sie jedoch, dass Microsoft Word Online ein Dokument, das mit einem Nicht‑GUID‑Wert erstellt wurde, nicht öffnen kann. Daher wird für diese Eigenschaft bevorzugt eine GUID verwendet.

Ein gültiger Wert muss ein Bezeichner sein, der unter allen benutzerdefinierten XML‑Daten‑Teilen in diesem Dokument eindeutig ist.

Der Standardwert ist eine leere Zeichenkette. Der Wert darf nicht null sein.

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
| Wert | java.lang.String | Die Zeichenkette, die diesen benutzerdefinierten XML‑Teil innerhalb eines OOXML‑Dokuments identifiziert. |

