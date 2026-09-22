---
title: "XmlMapping"
linktitle: "XmlMapping"
second_title: "Aspose.Words لـ Java"
description: "يحدد المعلومات التي تُستخدم لإنشاء ربط بين وسم المستند الهيكلي الأصلي وعنصر XML مخزن داخل جزء بيانات XML مخصص في المستند في Java."
type: docs
weight: 748
url: /ar/java/com.aspose.words/xmlmapping/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class XmlMapping implements Cloneable
```

يحدد المعلومات المستخدمة لإنشاء ربط بين علامة المستند المهيكلة الأصلية وعنصر XML المخزن داخل جزء بيانات XML مخصص في المستند.

لمزيد من المعلومات، زر مقالة الوثائق [ Structured Document Tags or Content Control ][Structured Document Tags or Content Control].

 **Examples:** 

يوضح كيفية تعيين ربط XML لأجزاء XML مخصصة.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [delete()](#delete) | يحذف ربط المستند الهيكلي الأصلي ببيانات XML. |
| [getCustomXmlPart()](#getCustomXmlPart) | يرجع جزء بيانات XML المخصص الذي يتم ربط وسم المستند الهيكلي الأصلي به. |
| [getPrefixMappings()](#getPrefixMappings) | يرجع ربط بادئات مساحة اسم XML لتقييم [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath). |
| [getStoreItemId()](#getStoreItemId) | يحدد معرف بيانات XML المخصص لجزء بيانات XML المخصص الذي سيُستخدم لتقييم تعبير [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath). |
| [getXPath()](#getXPath) | يرجع تعبير XPath الذي يتم تقييمه للعثور على عقدة XML المخصصة التي تم ربطها بوسم المستند الهيكلي الأصلي. |
| [isMapped()](#isMapped) | يرجع  true  إذا تم ربط وسم المستند الهيكلي الأصلي بنجاح ببيانات XML. |
| [setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping)](#setMapping-com.aspose.words.CustomXmlPart-java.lang.String-java.lang.String) | يضبط ربطًا بين وسم المستند الهيكلي الأصلي وعقدة XML لجزء بيانات XML مخصص. |
### delete() {#delete}
```
public void delete()
```


يحذف ربط المستند الهيكلي الأصلي ببيانات XML.

 **Examples:** 

يوضح كيفية تعيين ربط XML لأجزاء XML مخصصة.

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


يرجع جزء بيانات XML المخصص الذي يتم ربط وسم المستند الهيكلي الأصلي به.

 **Examples:** 

يوضح كيفية تعيين ربط XML لأجزاء XML مخصصة.

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


يرجع ربط بادئات مساحة اسم XML لتقييم [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath).

 **Remarks:** 

يحدد مجموعة ربط البادئات التي ستُستخدم لتفسير تعبير XPath عندما يتم تقييم تعبير XPath مقابل أجزاء بيانات XML المخصصة في المستند.

 **Examples:** 

يوضح كيفية تعيين ربط XML لأجزاء XML مخصصة.

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
java.lang.String - ربط بادئات مساحة اسم XML لتقييم [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath).
### getStoreItemId() {#getStoreItemId}
```
public String getStoreItemId()
```


يحدد معرف بيانات XML المخصص لجزء بيانات XML المخصص الذي سيُستخدم لتقييم تعبير [getXPath()](../../com.aspose.words/xmlmapping/\#getXPath).

 **Examples:** 

يوضح كيفية الحصول على معرف بيانات XML المخصص لجزء XML.

```

 Document doc = new Document(getMyDir() + "Custom XML part in structured document tag.docx");

 // Structured document tags have IDs in the form of GUIDs.
 StructuredDocumentTag tag = (StructuredDocumentTag) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG, 0, true);

 Assert.assertEquals("{F3029283-4FF8-4DD2-9F31-395F19ACEE85}", tag.getXmlMapping().getStoreItemId());
 
```

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getXPath() {#getXPath}
```
public String getXPath()
```


يرجع تعبير XPath الذي يتم تقييمه للعثور على عقدة XML المخصصة التي تم ربطها بوسم المستند الهيكلي الأصلي.

 **Examples:** 

يوضح كيفية تعيين ربط XML لأجزاء XML مخصصة.

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
java.lang.String - تعبير XPath الذي يتم تقييمه للعثور على عقدة XML المخصصة التي تم ربطها بوسم المستند الهيكلي الأصلي.
### isMapped() {#isMapped}
```
public boolean isMapped()
```


يرجع  true  إذا تم ربط وسم المستند الهيكلي الأصلي بنجاح ببيانات XML.

 **Examples:** 

يوضح كيفية تعيين ربط XML لأجزاء XML مخصصة.

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
boolean -  true  إذا تم ربط وسم المستند الهيكلي الأصلي بنجاح ببيانات XML.
### setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping) {#setMapping-com.aspose.words.CustomXmlPart-java.lang.String-java.lang.String}
```
public boolean setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping)
```


يضبط ربطًا بين وسم المستند الهيكلي الأصلي وعقدة XML لجزء بيانات XML مخصص.

 **Examples:** 

يوضح كيفية إنشاء علامة مستند مُنظم ببيانات XML مخصصة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| customXmlPart | [CustomXmlPart](../../com.aspose.words/customxmlpart/) | جزء بيانات XML مخصص للربط به. |
| xPath | java.lang.String | تعبير XPath للعثور على عقدة XML. |
| prefixMapping | java.lang.String | تعيينات بادئة مساحة الاسم XML لتقييم XPath. |

**Returns:**
منطقي - علامة تشير إلى ما إذا كان وسم المستند المهيكل الأب قد تم ربطه بنجاح بعقدة XML.
