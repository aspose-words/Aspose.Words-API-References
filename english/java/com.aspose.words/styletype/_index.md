---
title: StyleType
linktitle: StyleType
second_title: Aspose.Words for Java
description: Represents type of the style in Java.
type: docs
weight: 641
url: /java/com.aspose.words/styletype/
---

**Inheritance:**
java.lang.Object
```
public class StyleType
```

Represents type of the style.

 **Examples:** 

Shows how to create a list style and use it in a document.

```

 Document doc = new Document();

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // We can contain an entire List object within a style.
 Style listStyle = doc.getStyles().add(StyleType.LIST, "MyListStyle");

 List list1 = listStyle.getList();

 Assert.assertTrue(list1.isListStyleDefinition());
 Assert.assertFalse(list1.isListStyleReference());
 Assert.assertTrue(list1.isMultiLevel());
 Assert.assertEquals(listStyle, list1.getStyle());

 // Change the appearance of all list levels in our list.
 for (ListLevel level : list1.getListLevels()) {
     level.getFont().setName("Verdana");
     level.getFont().setColor(Color.BLUE);
     level.getFont().setBold(true);
 }

 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Using list style first time:");

 // Create another list from a list within a style.
 List list2 = doc.getLists().add(listStyle);

 Assert.assertFalse(list2.isListStyleDefinition());
 Assert.assertTrue(list2.isListStyleReference());
 Assert.assertEquals(listStyle, list2.getStyle());

 // Add some list items that our list will format.
 builder.getListFormat().setList(list2);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 builder.writeln("Using list style second time:");

 // Create and apply another list based on the list style.
 List list3 = doc.getLists().add(listStyle);
 builder.getListFormat().setList(list3);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 builder.getDocument().save(getArtifactsDir() + "Lists.CreateAndUseListStyle.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [CHARACTER](#CHARACTER) | The style is a character style. |
| [LIST](#LIST) | The style is a list style. |
| [PARAGRAPH](#PARAGRAPH) | The style is a paragraph style. |
| [TABLE](#TABLE) | The style is a table style. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String styleTypeName)](#fromName-java.lang.String) |  |
| [getName(int styleType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int styleType)](#toString-int) |  |
### CHARACTER {#CHARACTER}
```
public static int CHARACTER
```


The style is a character style.

### LIST {#LIST}
```
public static int LIST
```


The style is a list style.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


The style is a paragraph style.

### TABLE {#TABLE}
```
public static int TABLE
```


The style is a table style.

### length {#length}
```
public static int length
```


### fromName(String styleTypeName) {#fromName-java.lang.String}
```
public static int fromName(String styleTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| styleTypeName | java.lang.String |  |

**Returns:**
int
### getName(int styleType) {#getName-int}
```
public static String getName(int styleType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| styleType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int styleType) {#toString-int}
```
public static String toString(int styleType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| styleType | int |  |

**Returns:**
java.lang.String
