---
title: ListLevelCollection
linktitle: ListLevelCollection
second_title: Aspose.Words for Java
description: A collection of list formatting for each level in a list in Java.
type: docs
weight: 425
url: /java/com.aspose.words/listlevelcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class ListLevelCollection implements Cloneable, Iterable
```

A collection of list formatting for each level in a list.

To learn more, visit the [ Working with Lists ][Working with Lists] documentation article.

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

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```

 Document doc = new Document();

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create a list from a Microsoft Word template, and customize the first two of its list levels.
 List list = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 ListLevel listLevel = list.getListLevels().get(0);
 listLevel.getFont().setColor(Color.RED);
 listLevel.getFont().setSize(24.0);
 listLevel.setNumberStyle(NumberStyle.ORDINAL_TEXT);
 listLevel.setStartAt(21);
 listLevel.setNumberFormat(" ");

 listLevel.setNumberPosition(-36);
 listLevel.setTextPosition(144.0);
 listLevel.setTabPosition(144.0);

 listLevel = list.getListLevels().get(1);
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

 builder.getListFormat().setList(list);
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


[Working with Lists]: https://docs.aspose.com/words/java/working-with-lists/
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int) | Gets a list level by index. |
| [getCount()](#getCount) | Gets the number of levels in this list. |
| [iterator()](#iterator) | Gets the enumerator object that will enumerate levels in this list. |
| [set(int index, ListLevel value)](#set-int-com.aspose.words.ListLevel) | Gets a list level by index. |
### get(int index) {#get-int}
```
public ListLevel get(int index)
```


Gets a list level by index.

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

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```

 Document doc = new Document();

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create a list from a Microsoft Word template, and customize the first two of its list levels.
 List list = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 ListLevel listLevel = list.getListLevels().get(0);
 listLevel.getFont().setColor(Color.RED);
 listLevel.getFont().setSize(24.0);
 listLevel.setNumberStyle(NumberStyle.ORDINAL_TEXT);
 listLevel.setStartAt(21);
 listLevel.setNumberFormat(" ");

 listLevel.setNumberPosition(-36);
 listLevel.setTextPosition(144.0);
 listLevel.setTabPosition(144.0);

 listLevel = list.getListLevels().get(1);
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

 builder.getListFormat().setList(list);
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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[ListLevel](../../com.aspose.words/listlevel/) - A list level by index.
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of levels in this list.

 **Remarks:** 

There could be 1 or 9 levels in a list.

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

**Returns:**
int - The number of levels in this list.
### iterator() {#iterator}
```
public Iterator iterator()
```


Gets the enumerator object that will enumerate levels in this list.

 **Examples:** 

Shows advances ways of customizing list labels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 List list = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 // Level 1 labels will be formatted according to the "Heading 1" paragraph style and will have a prefix.
 // These will look like "Appendix A", "Appendix B"...
 list.getListLevels().get(0).setNumberFormat("Appendix  ");
 list.getListLevels().get(0).setNumberStyle(NumberStyle.UPPERCASE_LETTER);
 list.getListLevels().get(0).setLinkedStyle(doc.getStyles().get("Heading 1"));

 // Level 2 labels will display the current numbers of the first and the second list levels and have leading zeroes.
 // If the first list level is at 1, then the list labels from these will look like "Section (1.01)", "Section (1.02)"...
 list.getListLevels().get(1).setNumberFormat("Section ( .)");
 list.getListLevels().get(1).setNumberStyle(NumberStyle.LEADING_ZERO);

 // Note that the higher-level uses UppercaseLetter numbering.
 // We can set the "IsLegal" property to use Arabic numbers for the higher list levels.
 list.getListLevels().get(1).isLegal(true);
 list.getListLevels().get(1).setRestartAfterLevel(0);

 // Level 3 labels will be upper case Roman numerals with a prefix and a suffix and will restart at each List level 1 item.
 // These list labels will look like "-I-", "-II-"...
 list.getListLevels().get(2).setNumberFormat("--");
 list.getListLevels().get(2).setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 list.getListLevels().get(2).setRestartAfterLevel(1);

 // Make labels of all list levels bold.
 for (ListLevel level : list.getListLevels())
     level.getFont().setBold(true);

 // Apply list formatting to the current paragraph.
 builder.getListFormat().setList(list);

 // Create list items that will display all three of our list levels.
 for (int n = 0; n < 2; n++) {
     for (int i = 0; i < 3; i++) {
         builder.getListFormat().setListLevelNumber(i);
         builder.writeln("Level " + i);
     }
 }

 builder.getListFormat().removeNumbers();

 doc.save(getArtifactsDir() + "Lists.CreateListRestartAfterHigher.docx");
 
```

**Returns:**
java.util.Iterator
### set(int index, ListLevel value) {#set-int-com.aspose.words.ListLevel}
```
public void set(int index, ListLevel value)
```


Gets a list level by index.

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

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```

 Document doc = new Document();

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create a list from a Microsoft Word template, and customize the first two of its list levels.
 List list = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 ListLevel listLevel = list.getListLevels().get(0);
 listLevel.getFont().setColor(Color.RED);
 listLevel.getFont().setSize(24.0);
 listLevel.setNumberStyle(NumberStyle.ORDINAL_TEXT);
 listLevel.setStartAt(21);
 listLevel.setNumberFormat(" ");

 listLevel.setNumberPosition(-36);
 listLevel.setTextPosition(144.0);
 listLevel.setTabPosition(144.0);

 listLevel = list.getListLevels().get(1);
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

 builder.getListFormat().setList(list);
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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| value | [ListLevel](../../com.aspose.words/listlevel/) | A list level by index. |

