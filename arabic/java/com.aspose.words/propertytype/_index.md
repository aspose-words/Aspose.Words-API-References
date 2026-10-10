---
title: "PropertyType"
linktitle: "PropertyType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع البيانات لخاصية المستند في Java."
type: docs
weight: 555
url: /ar/java/com.aspose.words/propertytype/
---

**Inheritance:**
java.lang.Object
```
public class PropertyType
```

يحدد نوع البيانات لخاصية المستند.

 **Examples:** 

يوضح كيفية العمل مع خصائص المستند المخصصة.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [BOOLEAN](#BOOLEAN) | الخاصية هي قيمة منطقية. |
| [BYTE_ARRAY](#BYTE-ARRAY) | الخاصية هي مصفوفة من البايتات. |
| [DATE_TIME](#DATE-TIME) | الخاصية هي قيمة تاريخ ووقت. |
| [DOUBLE](#DOUBLE) | الخاصية هي عدد عائم. |
| [NUMBER](#NUMBER) | الخاصية هي عدد صحيح. |
| [OBJECT_ARRAY](#OBJECT-ARRAY) | الخاصية هي مصفوفة من الكائنات. |
| [OTHER](#OTHER) | الخاصية هي نوع آخر. |
| [STRING](#STRING) | الخاصية هي قيمة سلسلة. |
| [STRING_ARRAY](#STRING-ARRAY) | الخاصية هي مصفوفة من السلاسل. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String propertyTypeName)](#fromName-java.lang.String) |  |
| [getName(int propertyType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int propertyType)](#toString-int) |  |
### BOOLEAN {#BOOLEAN}
```
public static int BOOLEAN
```


الخاصية هي قيمة منطقية.

### BYTE_ARRAY {#BYTE-ARRAY}
```
public static int BYTE_ARRAY
```


الخاصية هي مصفوفة من البايتات.

### DATE_TIME {#DATE-TIME}
```
public static int DATE_TIME
```


الخاصية هي قيمة تاريخ ووقت.

### DOUBLE {#DOUBLE}
```
public static int DOUBLE
```


الخاصية هي عدد عائم.

### NUMBER {#NUMBER}
```
public static int NUMBER
```


الخاصية هي عدد صحيح.

### OBJECT_ARRAY {#OBJECT-ARRAY}
```
public static int OBJECT_ARRAY
```


الخاصية هي مصفوفة من الكائنات.

### OTHER {#OTHER}
```
public static int OTHER
```


الخاصية هي نوع آخر.

### STRING {#STRING}
```
public static int STRING
```


الخاصية هي قيمة سلسلة.

### STRING_ARRAY {#STRING-ARRAY}
```
public static int STRING_ARRAY
```


الخاصية هي مصفوفة من السلاسل.

### length {#length}
```
public static int length
```


### fromName(String propertyTypeName) {#fromName-java.lang.String}
```
public static int fromName(String propertyTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| propertyTypeName | java.lang.String |  |

**Returns:**
int
### getName(int propertyType) {#getName-int}
```
public static String getName(int propertyType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| propertyType | int |  |

**Returns:**
java.lang.String
