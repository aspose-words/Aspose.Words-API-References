---
title: XmlMapping
second_title: Aspose.Words for Java API Reference
description: Specifies the information that is used to establish a mapping between the parent structured document tag and an XML element stored within a custom XML data part in the document.
type: docs
weight: 629
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

To learn more, visit the **Structured Document Tags or Content Control** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping)](#setMapping-com.aspose.words.CustomXmlPart-java.lang.String-java.lang.String-) | Sets a mapping between the parent structured document tag and an XML node of a custom XML data part. |
| [delete()](#delete--) | Deletes mapping of the parent structured document to XML data. |
| [getPrefixMappings()](#getPrefixMappings--) | Returns XML namespace prefix mappings to evaluate the [getXPath()](../../com.aspose.words/xmlmapping\#getXPath--). |
| [getXPath()](#getXPath--) | Returns the XPath expression, which is evaluated to find the custom XML node that is mapped to the parent structured document tag. |
| [getCustomXmlPart()](#getCustomXmlPart--) | Returns the custom XML data part to which the parent structured document tag is mapped. |
| [isMapped()](#isMapped--) | Returns **true** if the parent structured document tag is successfully mapped to XML data. |
| [getStoreItemId()](#getStoreItemId--) | Specifies the custom XML data identifier for the custom XML data part which shall be used to evaluate the [getXPath()](../../com.aspose.words/xmlmapping\#getXPath--) expression. |
### setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping) {#setMapping-com.aspose.words.CustomXmlPart-java.lang.String-java.lang.String-}
```
public boolean setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping)
```


Sets a mapping between the parent structured document tag and an XML node of a custom XML data part.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| customXmlPart | [CustomXmlPart](../../com.aspose.words/customxmlpart) | A custom XML data part to map to. |
| xPath | java.lang.String | An XPath expression to find the XML node. |
| prefixMapping | java.lang.String | XML namespace prefix mappings to evaluate the XPath. |

**Returns:**
boolean - A flag indicating whether the parent structured document tag is successfully mapped to the XML node.
### delete() {#delete--}
```
public void delete()
```


Deletes mapping of the parent structured document to XML data.

### getPrefixMappings() {#getPrefixMappings--}
```
public String getPrefixMappings()
```


Returns XML namespace prefix mappings to evaluate the [getXPath()](../../com.aspose.words/xmlmapping\#getXPath--). Specifies the set of prefix mappings, which shall be used to interpret the XPath expression when the XPath expression is evaluated against the custom XML data parts in the document.

**Returns:**
java.lang.String - XML namespace prefix mappings to evaluate the [getXPath()](../../com.aspose.words/xmlmapping\#getXPath--).
### getXPath() {#getXPath--}
```
public String getXPath()
```


Returns the XPath expression, which is evaluated to find the custom XML node that is mapped to the parent structured document tag.

**Returns:**
java.lang.String - The XPath expression, which is evaluated to find the custom XML node that is mapped to the parent structured document tag.
### getCustomXmlPart() {#getCustomXmlPart--}
```
public CustomXmlPart getCustomXmlPart()
```


Returns the custom XML data part to which the parent structured document tag is mapped.

**Returns:**
[CustomXmlPart](../../com.aspose.words/customxmlpart) - The custom XML data part to which the parent structured document tag is mapped.
### isMapped() {#isMapped--}
```
public boolean isMapped()
```


Returns **true** if the parent structured document tag is successfully mapped to XML data.

**Returns:**
boolean - **true** if the parent structured document tag is successfully mapped to XML data.
### getStoreItemId() {#getStoreItemId--}
```
public String getStoreItemId()
```


Specifies the custom XML data identifier for the custom XML data part which shall be used to evaluate the [getXPath()](../../com.aspose.words/xmlmapping\#getXPath--) expression.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
