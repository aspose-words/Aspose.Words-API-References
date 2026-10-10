---
title: "StyleType"
linktitle: "StyleType"
second_title: "Aspose.Words für Java"
description: "Stellt den Typ des Stils in Java dar."
type: docs
weight: 644
url: /de/java/com.aspose.words/styletype/
---

**Inheritance:**
java.lang.Object
```
public class StyleType
```

Stellt den Typ des Stils dar.

 **Examples:** 

Zeigt, wie man einen Liststil erstellt und in einem Dokument verwendet.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CHARACTER](#CHARACTER) | Der Stil ist ein Zeichenstil. |
| [LIST](#LIST) | Der Stil ist ein Listenstil. |
| [PARAGRAPH](#PARAGRAPH) | Der Stil ist ein Absatzstil. |
| [TABLE](#TABLE) | Der Stil ist ein Tabellenstil. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String styleTypeName)](#fromName-java.lang.String) |  |
| [getName(int styleType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int styleType)](#toString-int) |  |
### CHARACTER {#CHARACTER}
```
public static int CHARACTER
```


Der Stil ist ein Zeichenstil.

### LIST {#LIST}
```
public static int LIST
```


Der Stil ist ein Listenstil.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


Der Stil ist ein Absatzstil.

### TABLE {#TABLE}
```
public static int TABLE
```


Der Stil ist ein Tabellenstil.

### length {#length}
```
public static int length
```


### fromName(String styleTypeName) {#fromName-java.lang.String}
```
public static int fromName(String styleTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| styleTypeName | java.lang.String |  |

**Returns:**
int
### getName(int styleType) {#getName-int}
```
public static String getName(int styleType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| styleType | int |  |

**Returns:**
java.lang.String
