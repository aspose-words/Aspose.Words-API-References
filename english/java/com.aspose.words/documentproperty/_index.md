---
title: DocumentProperty
second_title: Aspose.Words for Java API Reference
description: Represents a custom or built-in document property.
type: docs
weight: 126
url: /java/com.aspose.words/documentproperty/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class DocumentProperty implements Cloneable
```

Represents a custom or built-in document property.

To learn more, visit the **Work with Document Properties** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getName()](#getName--) | Returns the name of the property. |
| [getValue()](#getValue--) | Gets the value of the property. |
| [setValue(Object value)](#setValue-java.lang.Object-) | Sets the value of the property. |
| [getType()](#getType--) | Gets the data type of the property. |
| [getLinkSource()](#getLinkSource--) | Gets the source of a linked custom document property. |
| [isLinkToContent()](#isLinkToContent--) | Shows whether this property is linked to content or not. |
| [toString()](#toString--) | Returns the property value as a string formatted according to the current locale. |
| [toInt()](#toInt--) | Returns the property value as integer. |
| [toDouble()](#toDouble--) | Returns the property value as double. |
| [toDateTime()](#toDateTime--) | Returns the property value as DateTime in UTC. |
| [toBool()](#toBool--) | Returns the property value as bool. |
| [toByteArray()](#toByteArray--) | Returns the property value as byte array. |
### getName() {#getName--}
```
public String getName()
```


Returns the name of the property.

Cannot be null and cannot be an empty string.

**Returns:**
java.lang.String - The name of the property.
### getValue() {#getValue--}
```
public Object getValue()
```


Gets the value of the property.

Cannot be null.

**Returns:**
java.lang.Object - The value of the property.
### setValue(Object value) {#setValue-java.lang.Object-}
```
public void setValue(Object value)
```


Sets the value of the property.

Cannot be null.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.Object | The value of the property. |

### getType() {#getType--}
```
public int getType()
```


Gets the data type of the property.

**Returns:**
int - The data type of the property. The returned value is one of [PropertyType](../../com.aspose.words/propertytype) constants.
### getLinkSource() {#getLinkSource--}
```
public String getLinkSource()
```


Gets the source of a linked custom document property.

**Returns:**
java.lang.String - The source of a linked custom document property.
### isLinkToContent() {#isLinkToContent--}
```
public boolean isLinkToContent()
```


Shows whether this property is linked to content or not.

**Returns:**
boolean - The corresponding  boolean  value.
### toString() {#toString--}
```
public String toString()
```


Returns the property value as a string formatted according to the current locale.

Converts a boolean property into "Y" or "N". Converts a date property into a short date string. For all other types converts a property using Object.ToString().

**Returns:**
java.lang.String
### toInt() {#toInt--}
```
public int toInt()
```


Returns the property value as integer. Throws an exception if the property type is not [PropertyType.NUMBER](../../com.aspose.words/propertytype\#NUMBER).

**Returns:**
int
### toDouble() {#toDouble--}
```
public double toDouble()
```


Returns the property value as double. Throws an exception if the property type is not [PropertyType.NUMBER](../../com.aspose.words/propertytype\#NUMBER).

**Returns:**
double
### toDateTime() {#toDateTime--}
```
public Date toDateTime()
```


Returns the property value as DateTime in UTC.

Throws an exception if the property type is not [PropertyType.DATE\_TIME](../../com.aspose.words/propertytype\#DATE-TIME).

Microsoft Word stores only the date part (no time) for custom date properties.

**Returns:**
java.util.Date
### toBool() {#toBool--}
```
public boolean toBool()
```


Returns the property value as bool.

Throws an exception if the property type is not [PropertyType.BOOLEAN](../../com.aspose.words/propertytype\#BOOLEAN).

**Returns:**
boolean
### toByteArray() {#toByteArray--}
```
public byte[] toByteArray()
```


Returns the property value as byte array.

Throws an exception if the property type is not [PropertyType.BYTE\_ARRAY](../../com.aspose.words/propertytype\#BYTE-ARRAY).

**Returns:**
byte[]
