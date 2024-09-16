---
title: PropertyType
linktitle: PropertyType
second_title: Aspose.Words for Java
description: Specifies data type of a document property in Java.
type: docs
weight: 521
url: /java/com.aspose.words/propertytype/
---

**Inheritance:**
java.lang.Object
```
public class PropertyType
```

Specifies data type of a document property.

 **Examples:** 

Shows how to work with a document's custom properties.

```

 Document doc = new Document();
 CustomDocumentProperties properties = doc.getCustomDocumentProperties();

 Assert.assertEquals(0, properties.getCount());

 // Custom document properties are key-value pairs that we can add to the document.
 properties.add("Authorized", true);
 properties.add("Authorized By", "John Doe");
 properties.add("Authorized Date", new Date());
 properties.add("Authorized Revision", doc.getBuiltInDocumentProperties().getRevisionNumber());
 properties.add("Authorized Amount", 123.45);

 // The collection sorts the custom properties in alphabetic order.
 Assert.assertEquals(1, properties.indexOf("Authorized Amount"));
 Assert.assertEquals(5, properties.getCount());

 // Print every custom property in the document.
 Iterator enumerator = properties.iterator();
 while (enumerator.hasNext()) {
     DocumentProperty property = enumerator.next();
     System.out.println(MessageFormat.format("Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", property.getName(), property.getType(), property.getValue()));
 }

 // Display the value of a custom property using a DOCPROPERTY field.
 DocumentBuilder builder = new DocumentBuilder(doc);
 FieldDocProperty field = (FieldDocProperty) builder.insertField(" DOCPROPERTY \"Authorized By\"");
 field.update();

 Assert.assertEquals("John Doe", field.getResult());

 // We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
 doc.save(getArtifactsDir() + "DocumentProperties.DocumentPropertyCollection.docx");

 // Below are three ways or removing custom properties from a document.
 // 1 -  Remove by index:
 properties.removeAt(1);

 Assert.assertFalse(properties.contains("Authorized Amount"));
 Assert.assertEquals(4, properties.getCount());

 // 2 -  Remove by name:
 properties.remove("Authorized Revision");

 Assert.assertFalse(properties.contains("Authorized Revision"));
 Assert.assertEquals(3, properties.getCount());

 // 3 -  Empty the entire collection at once:
 properties.clear();

 Assert.assertEquals(0, properties.getCount());
 
```
## Fields

| Field | Description |
| --- | --- |
| [BOOLEAN](#BOOLEAN) | The property is a boolean value. |
| [BYTE_ARRAY](#BYTE-ARRAY) | The property is an array of bytes. |
| [DATE_TIME](#DATE-TIME) | The property is a date time value. |
| [DOUBLE](#DOUBLE) | The property is a floating number. |
| [NUMBER](#NUMBER) | The property is an integer number. |
| [OBJECT_ARRAY](#OBJECT-ARRAY) | The property is an array of objects. |
| [OTHER](#OTHER) | The property is some other type. |
| [STRING](#STRING) | The property is a string value. |
| [STRING_ARRAY](#STRING-ARRAY) | The property is an array of strings. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String propertyTypeName)](#fromName-java.lang.String) |  |
| [getName(int propertyType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int propertyType)](#toString-int) |  |
### BOOLEAN {#BOOLEAN}
```
public static int BOOLEAN
```


The property is a boolean value.

### BYTE_ARRAY {#BYTE-ARRAY}
```
public static int BYTE_ARRAY
```


The property is an array of bytes.

### DATE_TIME {#DATE-TIME}
```
public static int DATE_TIME
```


The property is a date time value.

### DOUBLE {#DOUBLE}
```
public static int DOUBLE
```


The property is a floating number.

### NUMBER {#NUMBER}
```
public static int NUMBER
```


The property is an integer number.

### OBJECT_ARRAY {#OBJECT-ARRAY}
```
public static int OBJECT_ARRAY
```


The property is an array of objects.

### OTHER {#OTHER}
```
public static int OTHER
```


The property is some other type.

### STRING {#STRING}
```
public static int STRING
```


The property is a string value.

### STRING_ARRAY {#STRING-ARRAY}
```
public static int STRING_ARRAY
```


The property is an array of strings.

### length {#length}
```
public static int length
```


### fromName(String propertyTypeName) {#fromName-java.lang.String}
```
public static int fromName(String propertyTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| propertyTypeName | java.lang.String |  |

**Returns:**
int
### getName(int propertyType) {#getName-int}
```
public static String getName(int propertyType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| propertyType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int propertyType) {#toString-int}
```
public static String toString(int propertyType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| propertyType | int |  |

**Returns:**
java.lang.String
