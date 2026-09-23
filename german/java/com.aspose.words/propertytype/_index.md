---
title: "PropertyType"
linktitle: "PropertyType"
second_title: "Aspose.Words für Java"
description: "Gibt den Datentyp einer Dokumenteigenschaft in Java an."
type: docs
weight: 555
url: /de/java/com.aspose.words/propertytype/
---

**Inheritance:**
java.lang.Object
```
public class PropertyType
```

Gibt den Datentyp einer Dokumenteneigenschaft an.

 **Examples:** 

Zeigt, wie man mit benutzerdefinierten Dokumenteneigenschaften arbeitet.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BOOLEAN](#BOOLEAN) | Die Eigenschaft ist ein boolescher Wert. |
| [BYTE_ARRAY](#BYTE-ARRAY) | Die Eigenschaft ist ein Byte-Array. |
| [DATE_TIME](#DATE-TIME) | Die Eigenschaft ist ein Datum‑Uhrzeit-Wert. |
| [DOUBLE](#DOUBLE) | Die Eigenschaft ist eine Gleitkommazahl. |
| [NUMBER](#NUMBER) | Die Eigenschaft ist eine Ganzzahl. |
| [OBJECT_ARRAY](#OBJECT-ARRAY) | Die Eigenschaft ist ein Objekt-Array. |
| [OTHER](#OTHER) | Die Eigenschaft ist ein anderer Typ. |
| [STRING](#STRING) | Die Eigenschaft ist ein Zeichenkettenwert. |
| [STRING_ARRAY](#STRING-ARRAY) | Die Eigenschaft ist ein Zeichenketten‑Array. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String propertyTypeName)](#fromName-java.lang.String) |  |
| [getName(int propertyType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int propertyType)](#toString-int) |  |
### BOOLEAN {#BOOLEAN}
```
public static int BOOLEAN
```


Die Eigenschaft ist ein boolescher Wert.

### BYTE_ARRAY {#BYTE-ARRAY}
```
public static int BYTE_ARRAY
```


Die Eigenschaft ist ein Byte-Array.

### DATE_TIME {#DATE-TIME}
```
public static int DATE_TIME
```


Die Eigenschaft ist ein Datum‑Uhrzeit-Wert.

### DOUBLE {#DOUBLE}
```
public static int DOUBLE
```


Die Eigenschaft ist eine Gleitkommazahl.

### NUMBER {#NUMBER}
```
public static int NUMBER
```


Die Eigenschaft ist eine Ganzzahl.

### OBJECT_ARRAY {#OBJECT-ARRAY}
```
public static int OBJECT_ARRAY
```


Die Eigenschaft ist ein Objekt-Array.

### OTHER {#OTHER}
```
public static int OTHER
```


Die Eigenschaft ist ein anderer Typ.

### STRING {#STRING}
```
public static int STRING
```


Die Eigenschaft ist ein Zeichenkettenwert.

### STRING_ARRAY {#STRING-ARRAY}
```
public static int STRING_ARRAY
```


Die Eigenschaft ist ein Zeichenketten‑Array.

### length {#length}
```
public static int length
```


### fromName(String propertyTypeName) {#fromName-java.lang.String}
```
public static int fromName(String propertyTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| propertyTypeName | java.lang.String |  |

**Returns:**
int
### getName(int propertyType) {#getName-int}
```
public static String getName(int propertyType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| propertyType | int |  |

**Returns:**
java.lang.String
