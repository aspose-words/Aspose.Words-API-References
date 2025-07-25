---
title: ListTrailingCharacter
linktitle: ListTrailingCharacter
second_title: Aspose.Words for Java
description: Specifies the character that separates the list label from the text of the paragraph in Java.
type: docs
weight: 427
url: /java/com.aspose.words/listtrailingcharacter/
---

**Inheritance:**
java.lang.Object
```
public class ListTrailingCharacter
```

Specifies the character that separates the list label from the text of the paragraph.

 **Remarks:** 

Used as a value for the [ListLevel.getTrailingCharacter()](../../com.aspose.words/listlevel/\#getTrailingCharacter) / [ListLevel.setTrailingCharacter(int)](../../com.aspose.words/listlevel/\#setTrailingCharacter-int) property.

 **Examples:** 

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```

 Document doc = new Document();

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create a list from a Microsoft Word template, and customize the first two of its list levels.
 List docList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 ListLevel listLevel = docList.getListLevels().get(0);
 listLevel.getFont().setColor(Color.RED);
 listLevel.getFont().setSize(24.0);
 listLevel.setNumberStyle(NumberStyle.ORDINAL_TEXT);
 listLevel.setStartAt(21);
 listLevel.setNumberFormat(" ");

 listLevel.setNumberPosition(-36);
 listLevel.setTextPosition(144.0);
 listLevel.setTabPosition(144.0);

 listLevel = docList.getListLevels().get(1);
 listLevel.setAlignment(ListLevelAlignment.RIGHT);
 listLevel.setNumberStyle(NumberStyle.BULLET);
 listLevel.getFont().setName("Wingdings");
 listLevel.getFont().setColor(Color.BLUE);
 listLevel.getFont().setSize(24.0);

 // This NumberFormat value will create star-shaped bullet list symbols.
 listLevel.setNumberFormat("\uf0af");
 listLevel.setTrailingCharacter(ListTrailingCharacter.SPACE);
 listLevel.setNumberPosition(144.0);

 // Create paragraphs and apply both list levels of our custom list formatting to them.
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getListFormat().setList(docList);
 builder.writeln("The quick brown fox...");
 builder.writeln("The quick brown fox...");

 builder.getListFormat().listIndent();
 builder.writeln("jumped over the lazy dog.");
 builder.writeln("jumped over the lazy dog.");

 builder.getListFormat().listOutdent();
 builder.writeln("The quick brown fox...");

 builder.getListFormat().removeNumbers();

 builder.getDocument().save(getArtifactsDir() + "Lists.CreateCustomList.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [NOTHING](#NOTHING) | There is no separator character between the list label and text of the paragraph. |
| [SPACE](#SPACE) | A space character is placed between the list label and text of the paragraph. |
| [TAB](#TAB) | A tab character is placed between the list label and text of the paragraph. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String listTrailingCharacterName)](#fromName-java.lang.String) |  |
| [getName(int listTrailingCharacter)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int listTrailingCharacter)](#toString-int) |  |
### NOTHING {#NOTHING}
```
public static int NOTHING
```


There is no separator character between the list label and text of the paragraph.

### SPACE {#SPACE}
```
public static int SPACE
```


A space character is placed between the list label and text of the paragraph.

### TAB {#TAB}
```
public static int TAB
```


A tab character is placed between the list label and text of the paragraph.

### length {#length}
```
public static int length
```


### fromName(String listTrailingCharacterName) {#fromName-java.lang.String}
```
public static int fromName(String listTrailingCharacterName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| listTrailingCharacterName | java.lang.String |  |

**Returns:**
int
### getName(int listTrailingCharacter) {#getName-int}
```
public static String getName(int listTrailingCharacter)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| listTrailingCharacter | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int listTrailingCharacter) {#toString-int}
```
public static String toString(int listTrailingCharacter)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| listTrailingCharacter | int |  |

**Returns:**
java.lang.String
