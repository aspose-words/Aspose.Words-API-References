---
title: "XmlMapping"
linktitle: "XmlMapping"
second_title: "Aspose.Words для Java"
description: "Указывает информацию, используемую для установления сопоставления между тегом родительского структурированного документа и элементом XML, хранящимся в пользовательской части XML-данных в документе на Java."
type: docs
weight: 748
url: /ru/java/com.aspose.words/xmlmapping/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class XmlMapping implements Cloneable
```

Указывает информацию, используемую для установления сопоставления между родительским тегом структурированного документа и элементом XML, хранящимся в пользовательской части XML‑данных документа.

Чтобы узнать больше, посетите статью документации [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Examples:** 

Показывает, как установить сопоставления XML для пользовательских частей XML.

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
## Методы

| Метод | Описание |
| --- | --- |
| [delete()](#delete) | Удаляет сопоставление родительского структурированного документа с XML-данными. |
| [getCustomXmlPart()](#getCustomXmlPart) | Возвращает пользовательскую часть XML-данных, к которой сопоставлен тег родительского структурированного документа. |
| [getPrefixMappings()](#getPrefixMappings) | Возвращает сопоставления префиксов пространств имен XML для оценки [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath). |
| [getStoreItemId()](#getStoreItemId) | Указывает идентификатор пользовательских XML-данных для пользовательской части XML, который будет использоваться для оценки выражения [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath). |
| [getXPath()](#getXPath) | Возвращает выражение XPath, которое оценивается для поиска пользовательского узла XML, сопоставленного с тегом родительского структурированного документа. |
| [isMapped()](#isMapped) | Возвращает  true  если тег родительского структурированного документа успешно сопоставлен с XML-данными. |
| [setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping)](#setMapping-com.aspose.words.CustomXmlPart-java.lang.String-java.lang.String) | Устанавливает сопоставление между тегом родительского структурированного документа и узлом XML пользовательской части XML-данных. |
### delete() {#delete}
```
public void delete()
```


Удаляет сопоставление родительского структурированного документа с XML-данными.

 **Examples:** 

Показывает, как установить сопоставления XML для пользовательских частей XML.

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


Возвращает пользовательскую часть XML-данных, к которой сопоставлен тег родительского структурированного документа.

 **Examples:** 

Показывает, как установить сопоставления XML для пользовательских частей XML.

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


Возвращает сопоставления префиксов пространств имен XML для оценки [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath).

 **Remarks:** 

Указывает набор сопоставлений префиксов, которые будут использоваться для интерпретации выражения XPath, когда оно оценивается относительно пользовательских частей XML-данных в документе.

 **Examples:** 

Показывает, как установить сопоставления XML для пользовательских частей XML.

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
java.lang.String - сопоставления префиксов пространств имен XML для оценки [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath).
### getStoreItemId() {#getStoreItemId}
```
public String getStoreItemId()
```


Указывает идентификатор пользовательских XML-данных для пользовательской части XML, который будет использоваться для оценки выражения [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath).

 **Examples:** 

Показывает, как получить идентификатор пользовательских XML-данных XML-части.

```

 Document doc = new Document(getMyDir() + "Custom XML part in structured document tag.docx");

 // Structured document tags have IDs in the form of GUIDs.
 StructuredDocumentTag tag = (StructuredDocumentTag) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 0, true);

 Assert.assertEquals("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.getXmlMapping().getStoreItemId());
 
```

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### getXPath() {#getXPath}
```
public String getXPath()
```


Возвращает выражение XPath, которое оценивается для поиска пользовательского узла XML, сопоставленного с тегом родительского структурированного документа.

 **Examples:** 

Показывает, как установить сопоставления XML для пользовательских частей XML.

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
java.lang.String - выражение XPath, которое оценивается для поиска пользовательского узла XML, сопоставленного с тегом родительского структурированного документа.
### isMapped() {#isMapped}
```
public boolean isMapped()
```


Возвращает  true  если тег родительского структурированного документа успешно сопоставлен с XML-данными.

 **Examples:** 

Показывает, как установить сопоставления XML для пользовательских частей XML.

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
boolean -  true  если тег родительского структурированного документа успешно сопоставлен с XML-данными.
### setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping) {#setMapping-com.aspose.words.CustomXmlPart-java.lang.String-java.lang.String}
```
public boolean setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping)
```


Устанавливает сопоставление между тегом родительского структурированного документа и узлом XML пользовательской части XML-данных.

 **Examples:** 

Показывает, как создать структурированный тег документа с пользовательскими XML-данными.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| customXmlPart | [CustomXmlPart](../../com.aspose.words/customxmlpart/) | Пользовательская часть XML-данных для сопоставления. |
| xPath | java.lang.String | XPath-выражение для поиска узла XML. |
| prefixMapping | java.lang.String | Префиксы пространств имён XML для оценки XPath. |

**Returns:**
boolean — Флаг, указывающий, успешно ли родительский тег структурированного документа сопоставлен с узлом XML.
