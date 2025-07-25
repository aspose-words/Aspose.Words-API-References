---
title: List
linktitle: List
second_title: Aspose.Words for Java
description: Represents formatting of a list in Java.
type: docs
weight: 419
url: /java/com.aspose.words/list/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Comparable
```
public class List implements Cloneable, Comparable
```

Represents formatting of a list.

To learn more, visit the [ Working with Lists ][Working with Lists] documentation article.

 **Remarks:** 

A list in a Microsoft Word document is a set of list formatting properties. Each list can have up to 9 levels and formatting properties, such as number style, start value, indent, tab position etc are defined separately for each level.

A [List](../../com.aspose.words/list/) object always belongs to the [ListCollection](../../com.aspose.words/listcollection/) collection.

To create a new list, use the Add methods of the [ListCollection](../../com.aspose.words/listcollection/) collection.

To modify formatting of a list, use [ListLevel](../../com.aspose.words/listlevel/) objects found in the [getListLevels()](../../com.aspose.words/list/\#getListLevels) collection.

To apply or remove list formatting from a paragraph, use [ListFormat](../../com.aspose.words/listformat/).

 **Examples:** 

Shows how to restart numbering in a list by copying a list.

```

 Document doc = new Document();

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create a list from a Microsoft Word template, and customize its first list level.
 List list1 = doc.getLists().add(ListTemplate.NUMBER_ARABIC_PARENTHESIS);
 list1.getListLevels().get(0).getFont().setColor(Color.RED);
 list1.getListLevels().get(0).setAlignment(ListLevelAlignment.RIGHT);

 // Apply our list to some paragraphs.
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("List 1 starts below:");
 builder.getListFormat().setList(list1);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 // We can add a copy of an existing list to the document's list collection
 // to create a similar list without making changes to the original.
 List list2 = doc.getLists().addCopy(list1);
 list2.getListLevels().get(0).getFont().setColor(Color.BLUE);
 list2.getListLevels().get(0).setStartAt(10);

 // Apply the second list to new paragraphs.
 builder.writeln("List 2 starts below:");
 builder.getListFormat().setList(list2);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 doc.save(getArtifactsDir() + "Lists.RestartNumberingUsingListCopy.docx");
 
```

Shows how to work with list levels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Assert.assertFalse(builder.getListFormat().isListItem());

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Below are two types of lists that we can create using a document builder.
 // 1 -  A numbered list:
 // Numbered lists create a logical order for their paragraphs by numbering each item.
 builder.getListFormat().setList(doc.getLists().add(ListTemplate.NUMBER_DEFAULT));

 Assert.assertTrue(builder.getListFormat().isListItem());

 // By setting the "ListLevelNumber" property, we can increase the list level
 // to begin a self-contained sub-list at the current list item.
 // The Microsoft Word list template called "NumberDefault" uses numbers to create list levels for the first list level.
 // Deeper list levels use letters and lowercase Roman numerals.
 for (int i = 0; i < 9; i++) {
     builder.getListFormat().setListLevelNumber(i);
     builder.writeln("Level " + i);
 }

 // 2 -  A bulleted list:
 // This list will apply an indent and a bullet symbol ("\u2022") before each paragraph.
 // Deeper levels of this list will use different symbols, such as "\u25a0" and "\u25cb".
 builder.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));

 for (int i = 0; i < 9; i++) {
     builder.getListFormat().setListLevelNumber(i);
     builder.writeln("Level " + i);
 }

 // We can disable list formatting to not format any subsequent paragraphs as lists by un-setting the "List" flag.
 builder.getListFormat().setList(null);

 Assert.assertFalse(builder.getListFormat().isListItem());

 doc.save(getArtifactsDir() + "Lists.SpecifyListLevel.docx");
 
```

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


[Working with Lists]: https://docs.aspose.com/words/java/working-with-lists/
## Methods

| Method | Description |
| --- | --- |
| [compareTo(List other)](#compareTo-com.aspose.words.List) | Compares the specified list to the current list. |
| [equals(List list)](#equals-com.aspose.words.List) | Compares with the specified list. |
| [equals(Object obj)](#equals-java.lang.Object) | Determines whether the specified object is equal in value to the current object. |
| [getDocument()](#getDocument) | Gets the owner document. |
| [getListId()](#getListId) | Gets the unique identifier of the list. |
| [getListLevels()](#getListLevels) | Gets the collection of list levels for this list. |
| [getStyle()](#getStyle) | Gets the list style that this list references or defines. |
| [hasSameTemplate(List other)](#hasSameTemplate-com.aspose.words.List) | Returns true if the current list and the given list are created from the same template. |
| [hashCode()](#hashCode) |  |
| [isListStyleDefinition()](#isListStyleDefinition) | Returns  true  if this list is a definition of a list style. |
| [isListStyleReference()](#isListStyleReference) | Returns  true  if this list is a reference to a list style. |
| [isMultiLevel()](#isMultiLevel) | Returns  true  when the list contains 9 levels;  false  when 1 level. |
| [isRestartAtEachSection()](#isRestartAtEachSection) | Specifies whether list should be restarted at each section. |
| [isRestartAtEachSection(boolean value)](#isRestartAtEachSection-boolean) | Specifies whether list should be restarted at each section. |
### compareTo(List other) {#compareTo-com.aspose.words.List}
```
public int compareTo(List other)
```


Compares the specified list to the current list.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| other | [List](../../com.aspose.words/list/) |  |

**Returns:**
int
### equals(List list) {#equals-com.aspose.words.List}
```
public boolean equals(List list)
```


Compares with the specified list.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| list | [List](../../com.aspose.words/list/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Determines whether the specified object is equal in value to the current object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Gets the owner document.

 **Remarks:** 

A list always has a parent document and is valid only in the context of that document.

 **Examples:** 

Shows how to verify owner document properties of lists.

```

 Document doc = new Document();

 ListCollection lists = doc.getLists();

 Assert.assertEquals(doc, lists.getDocument());

 List docList = lists.add(ListTemplate.BULLET_DEFAULT);
 Assert.assertEquals(doc, docList.getDocument());

 System.out.println("Current list count: " + lists.getCount());
 System.out.println("Is the first document list: " + (lists.get(0).equals(docList)));
 System.out.println("ListId: " + docList.getListId());
 System.out.println("List is the same by ListId: " + (lists.getListByListId(1).equals(docList)));
 
```

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The owner document.
### getListId() {#getListId}
```
public int getListId()
```


Gets the unique identifier of the list.

 **Remarks:** 

You do not normally need to use this property. But if you use it, you normally do so in conjunction with the [ListCollection.getListByListId(int)](../../com.aspose.words/listcollection/\#getListByListId-int) method to find a list by its identifier.

 **Examples:** 

Shows how to verify owner document properties of lists.

```

 Document doc = new Document();

 ListCollection lists = doc.getLists();

 Assert.assertEquals(doc, lists.getDocument());

 List docList = lists.add(ListTemplate.BULLET_DEFAULT);
 Assert.assertEquals(doc, docList.getDocument());

 System.out.println("Current list count: " + lists.getCount());
 System.out.println("Is the first document list: " + (lists.get(0).equals(docList)));
 System.out.println("ListId: " + docList.getListId());
 System.out.println("List is the same by ListId: " + (lists.getListByListId(1).equals(docList)));
 
```

Shows how to output all paragraphs in a document that are list items.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getListFormat().applyNumberDefault();
 builder.writeln("Numbered list item 1");
 builder.writeln("Numbered list item 2");
 builder.writeln("Numbered list item 3");
 builder.getListFormat().removeNumbers();

 builder.getListFormat().applyBulletDefault();
 builder.writeln("Bulleted list item 1");
 builder.writeln("Bulleted list item 2");
 builder.writeln("Bulleted list item 3");
 builder.getListFormat().removeNumbers();

 NodeCollection paras = doc.getChildNodes(NodeType.PARAGRAPH, true);
 for (Paragraph para : (Iterable) paras) {
     if (para.getListFormat().isListItem()) {
         System.out.println(java.text.MessageFormat.format("*** A paragraph belongs to list {0}", para.getListFormat().getList().getListId()));
         System.out.println(para.getText());
     }
 }
 
```

**Returns:**
int - The unique identifier of the list.
### getListLevels() {#getListLevels}
```
public ListLevelCollection getListLevels()
```


Gets the collection of list levels for this list.

 **Remarks:** 

Use this property to access and modify formatting individual to each level of the list.

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

**Returns:**
[ListLevelCollection](../../com.aspose.words/listlevelcollection/) - The collection of list levels for this list.
### getStyle() {#getStyle}
```
public Style getStyle()
```


Gets the list style that this list references or defines.

 **Remarks:** 

If this list is not associated with a list style, the property will return  null .

A list could be a reference to a list style, in this case [isListStyleReference()](../../com.aspose.words/list/\#isListStyleReference) will be  true .

A list could be a definition of a list style, in this case [isListStyleDefinition()](../../com.aspose.words/list/\#isListStyleDefinition) will be  true . Such a list cannot be applied to paragraphs in the document directly.

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
[Style](../../com.aspose.words/style/) - The list style that this list references or defines.
### hasSameTemplate(List other) {#hasSameTemplate-com.aspose.words.List}
```
public boolean hasSameTemplate(List other)
```


Returns true if the current list and the given list are created from the same template.

 **Examples:** 

Shows how to define lists with the same ListDefId.

```

 Document doc = new Document(getMyDir() + "Different lists.docx");

 Assert.assertTrue(doc.getLists().get(0).hasSameTemplate(doc.getLists().get(1)));
 Assert.assertFalse(doc.getLists().get(1).hasSameTemplate(doc.getLists().get(2)));
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| other | [List](../../com.aspose.words/list/) |  |

**Returns:**
boolean
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isListStyleDefinition() {#isListStyleDefinition}
```
public boolean isListStyleDefinition()
```


Returns  true  if this list is a definition of a list style.

 **Remarks:** 

When this property is  true , the [getStyle()](../../com.aspose.words/list/\#getStyle) property returns the list style that this list defines.

By modifying properties of a list that defines a list style, you modify the properties of the list style.

A list that is a definition of a list style cannot be applied directly to paragraphs to make them numbered.

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
boolean -  true  if this list is a definition of a list style.
### isListStyleReference() {#isListStyleReference}
```
public boolean isListStyleReference()
```


Returns  true  if this list is a reference to a list style.

 **Remarks:** 

Note, modifying properties of a list that is a reference to list style has no effect. The list formatting specified in the list style itself always takes precedence.

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
boolean -  true  if this list is a reference to a list style.
### isMultiLevel() {#isMultiLevel}
```
public boolean isMultiLevel()
```


Returns  true  when the list contains 9 levels;  false  when 1 level.

 **Remarks:** 

The lists that you create with Aspose.Words are always multi-level lists and contain 9 levels.

Microsoft Word 2003 and later always create multi-level lists with 9 levels. But in some documents, created with earlier versions of Microsoft Word you might encounter lists that have 1 level only.

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
boolean -  true  when the list contains 9 levels;  false  when 1 level.
### isRestartAtEachSection() {#isRestartAtEachSection}
```
public boolean isRestartAtEachSection()
```


Specifies whether list should be restarted at each section. Default value is  false .

 **Remarks:** 

This option is supported only in RTF, DOC and DOCX document formats.

This option will be written to DOCX only if [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance/) is higher then [OoxmlCompliance.ECMA\_376\_2006](../../com.aspose.words/ooxmlcompliance/\#ECMA-376-2006).

 **Examples:** 

Shows how to configure a list to restart numbering at each section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 List list = doc.getLists().get(0);
 list.isRestartAtEachSection(restartListAtEachSection);

 // The "IsRestartAtEachSection" property will only be applicable when
 // the document's OOXML compliance level is to a standard that is newer than "OoxmlComplianceCore.Ecma376".
 OoxmlSaveOptions options = new OoxmlSaveOptions();
 {
     options.setCompliance(OoxmlCompliance.ISO_29500_2008_TRANSITIONAL);
 }

 builder.getListFormat().setList(list);

 builder.writeln("List item 1");
 builder.writeln("List item 2");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("List item 3");
 builder.writeln("List item 4");

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

 doc = new Document(getArtifactsDir() + "OoxmlSaveOptions.RestartingDocumentList.docx");

 Assert.assertEquals(restartListAtEachSection, doc.getLists().get(0).isRestartAtEachSection());
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### isRestartAtEachSection(boolean value) {#isRestartAtEachSection-boolean}
```
public void isRestartAtEachSection(boolean value)
```


Specifies whether list should be restarted at each section. Default value is  false .

 **Remarks:** 

This option is supported only in RTF, DOC and DOCX document formats.

This option will be written to DOCX only if [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance/) is higher then [OoxmlCompliance.ECMA\_376\_2006](../../com.aspose.words/ooxmlcompliance/\#ECMA-376-2006).

 **Examples:** 

Shows how to configure a list to restart numbering at each section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 List list = doc.getLists().get(0);
 list.isRestartAtEachSection(restartListAtEachSection);

 // The "IsRestartAtEachSection" property will only be applicable when
 // the document's OOXML compliance level is to a standard that is newer than "OoxmlComplianceCore.Ecma376".
 OoxmlSaveOptions options = new OoxmlSaveOptions();
 {
     options.setCompliance(OoxmlCompliance.ISO_29500_2008_TRANSITIONAL);
 }

 builder.getListFormat().setList(list);

 builder.writeln("List item 1");
 builder.writeln("List item 2");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("List item 3");
 builder.writeln("List item 4");

 doc.save(getArtifactsDir() + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

 doc = new Document(getArtifactsDir() + "OoxmlSaveOptions.RestartingDocumentList.docx");

 Assert.assertEquals(restartListAtEachSection, doc.getLists().get(0).isRestartAtEachSection());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

