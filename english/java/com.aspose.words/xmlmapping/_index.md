---
title: XmlMapping
second_title: Aspose.Words for Java API Reference
description: Specifies the information that is used to establish a mapping between the parent structured document tag and an XML element stored within a custom XML data part in the document.
type: docs
weight: 632
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


[Structured Document Tags or Content Control]: https://docs.aspose.com/words/java/structured-document-tags-or-content-control/
## Methods

| Method | Description |
| --- | --- |
| [delete()](#delete) | Deletes mapping of the parent structured document to XML data. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getCustomXmlPart()](#getCustomXmlPart) | Returns the custom XML data part to which the parent structured document tag is mapped. |
| [getPrefixMappings()](#getPrefixMappings) | Returns XML namespace prefix mappings to evaluate the [getXPath()](../../com.aspose.words/xmlmapping\#getXPath). |
| [getStoreItemId()](#getStoreItemId) | Specifies the custom XML data identifier for the custom XML data part which shall be used to evaluate the [getXPath()](../../com.aspose.words/xmlmapping\#getXPath) expression. |
| [getXPath()](#getXPath) | Returns the XPath expression, which is evaluated to find the custom XML node that is mapped to the parent structured document tag. |
| [hashCode()](#hashCode) |  |
| [isMapped()](#isMapped) | Returns  true  if the parent structured document tag is successfully mapped to XML data. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping)](#setMapping-com.aspose.words.CustomXmlPart-java.lang.String-java.lang.String) | Sets a mapping between the parent structured document tag and an XML node of a custom XML data part. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### delete() {#delete}
```
public void delete()
```


Deletes mapping of the parent structured document to XML data.

### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCustomXmlPart() {#getCustomXmlPart}
```
public CustomXmlPart getCustomXmlPart()
```


Returns the custom XML data part to which the parent structured document tag is mapped.

**Returns:**
[CustomXmlPart](../../com.aspose.words/customxmlpart) - The custom XML data part to which the parent structured document tag is mapped.
### getPrefixMappings() {#getPrefixMappings}
```
public String getPrefixMappings()
```


Returns XML namespace prefix mappings to evaluate the [getXPath()](../../com.aspose.words/xmlmapping\#getXPath). Specifies the set of prefix mappings, which shall be used to interpret the XPath expression when the XPath expression is evaluated against the custom XML data parts in the document.

**Returns:**
java.lang.String - XML namespace prefix mappings to evaluate the [getXPath()](../../com.aspose.words/xmlmapping\#getXPath).
### getStoreItemId() {#getStoreItemId}
```
public String getStoreItemId()
```


Specifies the custom XML data identifier for the custom XML data part which shall be used to evaluate the [getXPath()](../../com.aspose.words/xmlmapping\#getXPath) expression.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getXPath() {#getXPath}
```
public String getXPath()
```


Returns the XPath expression, which is evaluated to find the custom XML node that is mapped to the parent structured document tag.

**Returns:**
java.lang.String - The XPath expression, which is evaluated to find the custom XML node that is mapped to the parent structured document tag.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isMapped() {#isMapped}
```
public boolean isMapped()
```


Returns  true  if the parent structured document tag is successfully mapped to XML data.

**Returns:**
boolean - \{ true  if the parent structured document tag is successfully mapped to XML data.
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setMapping(CustomXmlPart customXmlPart, String xPath, String prefixMapping) {#setMapping-com.aspose.words.CustomXmlPart-java.lang.String-java.lang.String}
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
### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

