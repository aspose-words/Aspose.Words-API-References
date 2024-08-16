---
title: ListTemplate
linktitle: ListTemplate
second_title: Aspose.Words for Java
description: Specifies one of the predefined list formats available in Microsoft Word in Java.
type: docs
weight: 409
url: /java/com.aspose.words/listtemplate/
---

**Inheritance:**
java.lang.Object
```
public class ListTemplate
```

Specifies one of the predefined list formats available in Microsoft Word.

 **Remarks:** 

A list template value is used as a parameter into the **M:Aspose.Words.Lists.ListCollection.Add(Aspose.Words.Lists.ListTemplate)** method.

Aspose.Words list templates correspond to the 21 list templates available in the Bullets and Numbering dialog box in Microsoft Word 2003.

 **Examples:** 

Shows how to create a document that contains all outline headings list templates.

```

 public void outlineHeadingTemplates() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     List list = doc.getLists().add(ListTemplate.OUTLINE_HEADINGS_ARTICLE_SECTION);
     addOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Article Section\"");

     list = doc.getLists().add(ListTemplate.OUTLINE_HEADINGS_LEGAL);
     addOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Legal\"");

     builder.insertBreak(BreakType.PAGE_BREAK);

     list = doc.getLists().add(ListTemplate.OUTLINE_HEADINGS_NUMBERS);
     addOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Numbers\"");

     list = doc.getLists().add(ListTemplate.OUTLINE_HEADINGS_CHAPTER);
     addOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Chapters\"");

     doc.save(getArtifactsDir() + "Lists.OutlineHeadingTemplates.docx");
 }

 private static void addOutlineHeadingParagraphs(final DocumentBuilder builder, final List list, final String title) {
     builder.getParagraphFormat().clearFormatting();
     builder.writeln(title);

     for (int i = 0; i < 9; i++) {
         builder.getListFormat().setList(list);
         builder.getListFormat().setListLevelNumber(i);

         String styleName = "Heading " + (i + 1);
         builder.getParagraphFormat().setStyleName(styleName);
         builder.writeln(styleName);
     }

     builder.getListFormat().removeNumbers();
 }
 
```

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
## Fields

| Field | Description |
| --- | --- |
| [BULLET_ARROW_HEAD](#BULLET-ARROW-HEAD) | The bullet of the first level is an arrow head Wingding character. |
| [BULLET_CIRCLE](#BULLET-CIRCLE) | The bullet of the first level is a circle. |
| [BULLET_DEFAULT](#BULLET-DEFAULT) | Default bulleted list with 9 levels. |
| [BULLET_DIAMONDS](#BULLET-DIAMONDS) | The bullet of the first level is a 4-diamond Wingding character. |
| [BULLET_DISK](#BULLET-DISK) | Same as [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT). |
| [BULLET_SQUARE](#BULLET-SQUARE) | The bullet of the first level is a square. |
| [BULLET_TICK](#BULLET-TICK) | The bullet of the first level is a tick Wingding character. |
| [NUMBER_ARABIC_DOT](#NUMBER-ARABIC-DOT) | Same as [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT). |
| [NUMBER_ARABIC_PARENTHESIS](#NUMBER-ARABIC-PARENTHESIS) | The number of the first level is "1)". |
| [NUMBER_DEFAULT](#NUMBER-DEFAULT) | Default numbered list with 9 levels. |
| [NUMBER_LOWERCASE_LETTER_DOT](#NUMBER-LOWERCASE-LETTER-DOT) | The number of the first level is "a.". |
| [NUMBER_LOWERCASE_LETTER_PARENTHESIS](#NUMBER-LOWERCASE-LETTER-PARENTHESIS) | The number of the first level is "a)". |
| [NUMBER_LOWERCASE_ROMAN_DOT](#NUMBER-LOWERCASE-ROMAN-DOT) | The number of the first level is "i.". |
| [NUMBER_UPPERCASE_LETTER_DOT](#NUMBER-UPPERCASE-LETTER-DOT) | The number of the first level is "A.". |
| [NUMBER_UPPERCASE_ROMAN_DOT](#NUMBER-UPPERCASE-ROMAN-DOT) | The number of the first level is "I.". |
| [OUTLINE_BULLETS](#OUTLINE-BULLETS) | An outline lists with various bullets for different levels. |
| [OUTLINE_HEADINGS_ARTICLE_SECTION](#OUTLINE-HEADINGS-ARTICLE-SECTION) | An outline list with levels linked to Heading styles. |
| [OUTLINE_HEADINGS_CHAPTER](#OUTLINE-HEADINGS-CHAPTER) | An outline list with levels linked to Heading styles. |
| [OUTLINE_HEADINGS_LEGAL](#OUTLINE-HEADINGS-LEGAL) | An outline list with levels linked to Heading styles. |
| [OUTLINE_HEADINGS_NUMBERS](#OUTLINE-HEADINGS-NUMBERS) | An outline list with levels linked to Heading styles. |
| [OUTLINE_LEGAL](#OUTLINE-LEGAL) | An outline list with levels are numbered "1., 1.1., 1.1.1, ...". |
| [OUTLINE_NUMBERS](#OUTLINE-NUMBERS) | An outline list with levels numbered "1), a), i), (1), (a), (i), 1., a., i.". |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String listTemplateName)](#fromName-java.lang.String) |  |
| [getName(int listTemplate)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int listTemplate)](#toString-int) |  |
### BULLET_ARROW_HEAD {#BULLET-ARROW-HEAD}
```
public static int BULLET_ARROW_HEAD
```


The bullet of the first level is an arrow head Wingding character. The remaining levels are same as in [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Corresponds to the 6th bulleted list template in the Bullets and Numbering dialog box in Microsoft Word.

### BULLET_CIRCLE {#BULLET-CIRCLE}
```
public static int BULLET_CIRCLE
```


The bullet of the first level is a circle. The remaining levels are same as in [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Corresponds to the 2nd bulleted list template in the Bullets and Numbering dialog box in Microsoft Word.

### BULLET_DEFAULT {#BULLET-DEFAULT}
```
public static int BULLET_DEFAULT
```


Default bulleted list with 9 levels. Bullet of the first level is a disc, bullet of the second level is a circle, bullet of the third level is a square. Then formatting repeats for the remaining levels.

Each level is indented to the right by 0.25" relative to the previous level.

Corresponds to the 1st bulleted list template in the Bullets and Numbering dialog box in Microsoft Word.

### BULLET_DIAMONDS {#BULLET-DIAMONDS}
```
public static int BULLET_DIAMONDS
```


The bullet of the first level is a 4-diamond Wingding character. The remaining levels are same as in [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Corresponds to the 5th bulleted list template in the Bullets and Numbering dialog box in Microsoft Word.

### BULLET_DISK {#BULLET-DISK}
```
public static int BULLET_DISK
```


Same as [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Corresponds to the 1st bulleted list template in the Bullets and Numbering dialog box in Microsoft Word.

### BULLET_SQUARE {#BULLET-SQUARE}
```
public static int BULLET_SQUARE
```


The bullet of the first level is a square. The remaining levels are same as in [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Corresponds to the 3rd bulleted list template in the Bullets and Numbering dialog box in Microsoft Word.

### BULLET_TICK {#BULLET-TICK}
```
public static int BULLET_TICK
```


The bullet of the first level is a tick Wingding character. The remaining levels are same as in [BULLET\_DEFAULT](../../com.aspose.words/listtemplate/\#BULLET-DEFAULT).

Corresponds to the 7th bulleted list template in the Bullets and Numbering dialog box in Microsoft Word.

### NUMBER_ARABIC_DOT {#NUMBER-ARABIC-DOT}
```
public static int NUMBER_ARABIC_DOT
```


Same as [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corresponds to the 1st numbered list template in the Bullets and Numbering dialog box in Microsoft Word.

### NUMBER_ARABIC_PARENTHESIS {#NUMBER-ARABIC-PARENTHESIS}
```
public static int NUMBER_ARABIC_PARENTHESIS
```


The number of the first level is "1)". The remaining levels are same as in [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corresponds to the 2nd numbered list template in the Bullets and Numbering dialog box in Microsoft Word.

### NUMBER_DEFAULT {#NUMBER-DEFAULT}
```
public static int NUMBER_DEFAULT
```


Default numbered list with 9 levels. Arabic numbering (1., 2., 3., ...) for the first level, lowercase letter numbering (a., b., c., ...) for the second level, lowercase roman numbering (i., ii., iii., ...) for the third level. Then formatting repeats for the remaining levels.

Each level is indented to the right by 0.25" relative to the previous level.

Corresponds to the 1st numbered list template in the Bullets and Numbering dialog box in Microsoft Word.

### NUMBER_LOWERCASE_LETTER_DOT {#NUMBER-LOWERCASE-LETTER-DOT}
```
public static int NUMBER_LOWERCASE_LETTER_DOT
```


The number of the first level is "a.". The remaining levels are same as in [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corresponds to the 6th numbered list template in the Bullets and Numbering dialog box in Microsoft Word.

### NUMBER_LOWERCASE_LETTER_PARENTHESIS {#NUMBER-LOWERCASE-LETTER-PARENTHESIS}
```
public static int NUMBER_LOWERCASE_LETTER_PARENTHESIS
```


The number of the first level is "a)". The remaining levels are same as in [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corresponds to the 5th numbered list template in the Bullets and Numbering dialog box in Microsoft Word.

### NUMBER_LOWERCASE_ROMAN_DOT {#NUMBER-LOWERCASE-ROMAN-DOT}
```
public static int NUMBER_LOWERCASE_ROMAN_DOT
```


The number of the first level is "i.". The remaining levels are same as in [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corresponds to the 7th numbered list template in the Bullets and Numbering dialog box in Microsoft Word.

### NUMBER_UPPERCASE_LETTER_DOT {#NUMBER-UPPERCASE-LETTER-DOT}
```
public static int NUMBER_UPPERCASE_LETTER_DOT
```


The number of the first level is "A.". The remaining levels are same as in [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corresponds to the 4th numbered list template in the Bullets and Numbering dialog box in Microsoft Word.

### NUMBER_UPPERCASE_ROMAN_DOT {#NUMBER-UPPERCASE-ROMAN-DOT}
```
public static int NUMBER_UPPERCASE_ROMAN_DOT
```


The number of the first level is "I.". The remaining levels are same as in [NUMBER\_DEFAULT](../../com.aspose.words/listtemplate/\#NUMBER-DEFAULT).

Corresponds to the 3rd numbered list template in the Bullets and Numbering dialog box in Microsoft Word.

### OUTLINE_BULLETS {#OUTLINE-BULLETS}
```
public static int OUTLINE_BULLETS
```


An outline lists with various bullets for different levels.

Corresponds to the 3rd outline list template in the Bullets and Numbering dialog box in Microsoft Word.

### OUTLINE_HEADINGS_ARTICLE_SECTION {#OUTLINE-HEADINGS-ARTICLE-SECTION}
```
public static int OUTLINE_HEADINGS_ARTICLE_SECTION
```


An outline list with levels linked to Heading styles.

Corresponds to the 4th outline list template in the Bullets and Numbering dialog box in Microsoft Word.

### OUTLINE_HEADINGS_CHAPTER {#OUTLINE-HEADINGS-CHAPTER}
```
public static int OUTLINE_HEADINGS_CHAPTER
```


An outline list with levels linked to Heading styles.

Corresponds to the 7th outline list template in the Bullets and Numbering dialog box in Microsoft Word.

### OUTLINE_HEADINGS_LEGAL {#OUTLINE-HEADINGS-LEGAL}
```
public static int OUTLINE_HEADINGS_LEGAL
```


An outline list with levels linked to Heading styles.

Corresponds to the 5th outline list template in the Bullets and Numbering dialog box in Microsoft Word.

### OUTLINE_HEADINGS_NUMBERS {#OUTLINE-HEADINGS-NUMBERS}
```
public static int OUTLINE_HEADINGS_NUMBERS
```


An outline list with levels linked to Heading styles.

Corresponds to the 6th outline list template in the Bullets and Numbering dialog box in Microsoft Word.

### OUTLINE_LEGAL {#OUTLINE-LEGAL}
```
public static int OUTLINE_LEGAL
```


An outline list with levels are numbered "1., 1.1., 1.1.1, ...".

Corresponds to the 2nd outline list template in the Bullets and Numbering dialog box in Microsoft Word.

### OUTLINE_NUMBERS {#OUTLINE-NUMBERS}
```
public static int OUTLINE_NUMBERS
```


An outline list with levels numbered "1), a), i), (1), (a), (i), 1., a., i.".

Corresponds to the 1st outline list template in the Bullets and Numbering dialog box in Microsoft Word.

### length {#length}
```
public static int length
```


### fromName(String listTemplateName) {#fromName-java.lang.String}
```
public static int fromName(String listTemplateName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| listTemplateName | java.lang.String |  |

**Returns:**
int
### getName(int listTemplate) {#getName-int}
```
public static String getName(int listTemplate)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int listTemplate) {#toString-int}
```
public static String toString(int listTemplate)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| listTemplate | int |  |

**Returns:**
java.lang.String
