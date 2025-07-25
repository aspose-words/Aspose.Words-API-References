---
title: ListLevel
linktitle: ListLevel
second_title: Aspose.Words for Java
description: Defines formatting for a list level in Java.
type: docs
weight: 423
url: /java/com.aspose.words/listlevel/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ListLevel implements Cloneable
```

Defines formatting for a list level.

To learn more, visit the [ Working with Lists ][Working with Lists] documentation article.

 **Remarks:** 

You do not create objects of this class. List level objects are created automatically when a list is created. You access [ListLevel](../../com.aspose.words/listlevel/) objects via the [ListLevelCollection](../../com.aspose.words/listlevelcollection/) collection.

Use the properties of [ListLevel](../../com.aspose.words/listlevel/) to specify list formatting for individual list levels.

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


[Working with Lists]: https://docs.aspose.com/words/java/working-with-lists/
## Methods

| Method | Description |
| --- | --- |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [createPictureBullet()](#createPictureBullet) | Creates picture bullet shape for the current list level. |
| [deletePictureBullet()](#deletePictureBullet) | Deletes picture bullet for the current list level. |
| [equals(ListLevel level)](#equals-com.aspose.words.ListLevel) | Compares with the specified ListLevel. |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [getAlignment()](#getAlignment) | Gets the justification of the actual number of the list item. |
| [getCustomNumberStyleFormat()](#getCustomNumberStyleFormat) | Gets the custom number style format for this list level. |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getEffectiveValue(int index, int numberStyle, String customNumberStyleFormat)](#getEffectiveValue-int-int-java.lang.String) |  |
| [getFont()](#getFont) | Specifies character formatting used for the list label. |
| [getImageData()](#getImageData) | Returns image data of the picture bullet shape for the current list level. |
| [getLinkedStyle()](#getLinkedStyle) | Gets the paragraph style that is linked to this list level. |
| [getNumberFormat()](#getNumberFormat) | Gets the number format for the list level. |
| [getNumberPosition()](#getNumberPosition) | Gets the position (in points) of the number or bullet for the list level. |
| [getNumberStyle()](#getNumberStyle) | Gets the number style for this list level. |
| [getRestartAfterLevel()](#getRestartAfterLevel) | Gets the list level that must appear before the specified list level restarts numbering. |
| [getStartAt()](#getStartAt) | Gets the starting number for this list level. |
| [getTabPosition()](#getTabPosition) | Gets the tab position (in points) for the list level. |
| [getTextPosition()](#getTextPosition) | Gets the position (in points) for the second line of wrapping text for the list level. |
| [getTrailingCharacter()](#getTrailingCharacter) | Gets the character inserted after the number for the list level. |
| [hashCode()](#hashCode) |  |
| [isLegal()](#isLegal) | True if the level turns all inherited numbers to Arabic, false if it preserves their number style. |
| [isLegal(boolean value)](#isLegal-boolean) | True if the level turns all inherited numbers to Arabic, false if it preserves their number style. |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [setAlignment(int value)](#setAlignment-int) | Sets the justification of the actual number of the list item. |
| [setCustomNumberStyleFormat(String value)](#setCustomNumberStyleFormat-java.lang.String) | Sets the custom number style format for this list level. |
| [setLinkedStyle(Style value)](#setLinkedStyle-com.aspose.words.Style) | Sets the paragraph style that is linked to this list level. |
| [setNumberFormat(String value)](#setNumberFormat-java.lang.String) | Sets the number format for the list level. |
| [setNumberPosition(double value)](#setNumberPosition-double) | Sets the position (in points) of the number or bullet for the list level. |
| [setNumberStyle(int value)](#setNumberStyle-int) | Sets the number style for this list level. |
| [setRestartAfterLevel(int value)](#setRestartAfterLevel-int) | Sets the list level that must appear before the specified list level restarts numbering. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setStartAt(int value)](#setStartAt-int) | Sets the starting number for this list level. |
| [setTabPosition(double value)](#setTabPosition-double) | Sets the tab position (in points) for the list level. |
| [setTextPosition(double value)](#setTextPosition-double) | Sets the position (in points) for the second line of wrapping text for the list level. |
| [setTrailingCharacter(int value)](#setTrailingCharacter-int) | Sets the character inserted after the number for the list level. |
### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### createPictureBullet() {#createPictureBullet}
```
public void createPictureBullet()
```


Creates picture bullet shape for the current list level.

 **Remarks:** 

Please note, [getNumberStyle()](../../com.aspose.words/listlevel/\#getNumberStyle) / [setNumberStyle(int)](../../com.aspose.words/listlevel/\#setNumberStyle-int) will be set to [NumberStyle.BULLET](../../com.aspose.words/numberstyle/\#BULLET) and [getNumberFormat()](../../com.aspose.words/listlevel/\#getNumberFormat) / [setNumberFormat(java.lang.String)](../../com.aspose.words/listlevel/\#setNumberFormat-java.lang.String) to "\\xF0B7" to properly display picture bullet. Red cross image will be set as picture bullet image upon creating. To change it please use [getImageData()](../../com.aspose.words/listlevel/\#getImageData).

 **Examples:** 

Shows how to set a custom image icon for list item labels.

```

 Document doc = new Document();

 List docList = doc.getLists().add(ListTemplate.BULLET_CIRCLE);

 // Create a picture bullet for the current list level, and set an image from a local file system
 // as the icon that the bullets for this list level will display.
 docList.getListLevels().get(0).createPictureBullet();
 docList.getListLevels().get(0).getImageData().setImage(getImageDir() + "Logo icon.ico");

 Assert.assertTrue(docList.getListLevels().get(0).getImageData().hasImage());

 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getListFormat().setList(docList);
 builder.writeln("Hello world!");
 builder.write("Hello again!");

 doc.save(getArtifactsDir() + "Lists.CreatePictureBullet.docx");

 docList.getListLevels().get(0).deletePictureBullet();

 Assert.assertNull(docList.getListLevels().get(0).getImageData());
 
```

### deletePictureBullet() {#deletePictureBullet}
```
public void deletePictureBullet()
```


Deletes picture bullet for the current list level.

 **Remarks:** 

Default bullet will be shown after deleting.

 **Examples:** 

Shows how to set a custom image icon for list item labels.

```

 Document doc = new Document();

 List docList = doc.getLists().add(ListTemplate.BULLET_CIRCLE);

 // Create a picture bullet for the current list level, and set an image from a local file system
 // as the icon that the bullets for this list level will display.
 docList.getListLevels().get(0).createPictureBullet();
 docList.getListLevels().get(0).getImageData().setImage(getImageDir() + "Logo icon.ico");

 Assert.assertTrue(docList.getListLevels().get(0).getImageData().hasImage());

 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getListFormat().setList(docList);
 builder.writeln("Hello world!");
 builder.write("Hello again!");

 doc.save(getArtifactsDir() + "Lists.CreatePictureBullet.docx");

 docList.getListLevels().get(0).deletePictureBullet();

 Assert.assertNull(docList.getListLevels().get(0).getImageData());
 
```

### equals(ListLevel level) {#equals-com.aspose.words.ListLevel}
```
public boolean equals(ListLevel level)
```


Compares with the specified ListLevel.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| level | [ListLevel](../../com.aspose.words/listlevel/) |  |

**Returns:**
boolean
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Gets the justification of the actual number of the list item.

 **Remarks:** 

The list label is justified relative to the [getNumberPosition()](../../com.aspose.words/listlevel/\#getNumberPosition) / [setNumberPosition(double)](../../com.aspose.words/listlevel/\#setNumberPosition-double) property.

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
int - The justification of the actual number of the list item. The returned value is one of [ListLevelAlignment](../../com.aspose.words/listlevelalignment/) constants.
### getCustomNumberStyleFormat() {#getCustomNumberStyleFormat}
```
public String getCustomNumberStyleFormat()
```


Gets the custom number style format for this list level. For example: "a, �, \\u011d, ...".

 **Examples:** 

Shows how to get the format for a list with the custom number style.

```

 Document doc = new Document(getMyDir() + "List with leading zero.docx");

 ListLevel listLevel = doc.getFirstSection().getBody().getParagraphs().get(0).getListFormat().getListLevel();

 String customNumberStyleFormat = "";

 if (listLevel.getNumberStyle() == NumberStyle.CUSTOM)
     customNumberStyleFormat = listLevel.getCustomNumberStyleFormat();

 Assert.assertEquals("001, 002, 003, ...", customNumberStyleFormat);

 // We can get value for the specified index of the list item.
 Assert.assertEquals("iv", ListLevel.getEffectiveValue(4, NumberStyle.LOWERCASE_ROMAN, null));
 Assert.assertEquals("005", ListLevel.getEffectiveValue(5, NumberStyle.CUSTOM, customNumberStyleFormat));
 
```

Shows how to set customer number style format.

```

 Document doc = new Document(getMyDir() + "List with leading zero.docx");

 doc.updateListLabels();

 ParagraphCollection paras = doc.getFirstSection().getBody().getParagraphs();
 Assert.assertEquals("001.", paras.get(0).getListLabel().getLabelString());
 Assert.assertEquals("0001.", paras.get(1).getListLabel().getLabelString());
 Assert.assertEquals("0002.", paras.get(2).getListLabel().getLabelString());

 paras.get(1).getListFormat().getListLevel().setCustomNumberStyleFormat("001, 002, 003, ...");

 doc.updateListLabels();

 Assert.assertEquals("001.", paras.get(0).getListLabel().getLabelString());
 Assert.assertEquals("001.", paras.get(1).getListLabel().getLabelString());
 Assert.assertEquals("002.", paras.get(2).getListLabel().getLabelString());
 
```

**Returns:**
java.lang.String - The custom number style format for this list level.
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getEffectiveValue(int index, int numberStyle, String customNumberStyleFormat) {#getEffectiveValue-int-int-java.lang.String}
```
public static String getEffectiveValue(int index, int numberStyle, String customNumberStyleFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| numberStyle | int |  |
| customNumberStyleFormat | java.lang.String |  |

**Returns:**
java.lang.String
### getFont() {#getFont}
```
public Font getFont()
```


Specifies character formatting used for the list label.

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
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getImageData() {#getImageData}
```
public ImageData getImageData()
```


Returns image data of the picture bullet shape for the current list level.

 **Remarks:** 

If this level doesn't define picture bullet returns  null . Before setting new image for non picture bullet shape, please use [createPictureBullet()](../../com.aspose.words/listlevel/\#createPictureBullet) method first.

**Returns:**
[ImageData](../../com.aspose.words/imagedata/) - Image data of the picture bullet shape for the current list level.
### getLinkedStyle() {#getLinkedStyle}
```
public Style getLinkedStyle()
```


Gets the paragraph style that is linked to this list level.

 **Remarks:** 

This property is  null  when the list level is not linked to a paragraph style. This property can be set to  null .

 **Examples:** 

Shows advances ways of customizing list labels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 List docList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 // Level 1 labels will be formatted according to the "Heading 1" paragraph style and will have a prefix.
 // These will look like "Appendix A", "Appendix B"...
 docList.getListLevels().get(0).setNumberFormat("Appendix  ");
 docList.getListLevels().get(0).setNumberStyle(NumberStyle.UPPERCASE_LETTER);
 docList.getListLevels().get(0).setLinkedStyle(doc.getStyles().get("Heading 1"));

 // Level 2 labels will display the current numbers of the first and the second list levels and have leading zeroes.
 // If the first list level is at 1, then the list labels from these will look like "Section (1.01)", "Section (1.02)"...
 docList.getListLevels().get(1).setNumberFormat("Section ( .)");
 docList.getListLevels().get(1).setNumberStyle(NumberStyle.LEADING_ZERO);

 // Note that the higher-level uses UppercaseLetter numbering.
 // We can set the "IsLegal" property to use Arabic numbers for the higher list levels.
 docList.getListLevels().get(1).isLegal(true);
 docList.getListLevels().get(1).setRestartAfterLevel(0);

 // Level 3 labels will be upper case Roman numerals with a prefix and a suffix and will restart at each List level 1 item.
 // These list labels will look like "-I-", "-II-"...
 docList.getListLevels().get(2).setNumberFormat("--");
 docList.getListLevels().get(2).setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 docList.getListLevels().get(2).setRestartAfterLevel(1);

 // Make labels of all list levels bold.
 for (ListLevel level : docList.getListLevels())
     level.getFont().setBold(true);

 // Apply list formatting to the current paragraph.
 builder.getListFormat().setList(docList);

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
[Style](../../com.aspose.words/style/) - The paragraph style that is linked to this list level.
### getNumberFormat() {#getNumberFormat}
```
public String getNumberFormat()
```


Gets the number format for the list level.

 **Remarks:** 

Among normal text characters, the string can contain placeholder characters \\x0000 to \\x0008 representing the numbers from the corresponding list levels.

For example, the string "\\x0000.\\x0001)" will generate a list label that looks something like "1.5)". The number "1" is the current number from the 1st list level, the number "5" is the current number from the 2nd list level.

Null is not allowed, but an empty string meaning no number is valid.

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

Shows advances ways of customizing list labels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 List docList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 // Level 1 labels will be formatted according to the "Heading 1" paragraph style and will have a prefix.
 // These will look like "Appendix A", "Appendix B"...
 docList.getListLevels().get(0).setNumberFormat("Appendix  ");
 docList.getListLevels().get(0).setNumberStyle(NumberStyle.UPPERCASE_LETTER);
 docList.getListLevels().get(0).setLinkedStyle(doc.getStyles().get("Heading 1"));

 // Level 2 labels will display the current numbers of the first and the second list levels and have leading zeroes.
 // If the first list level is at 1, then the list labels from these will look like "Section (1.01)", "Section (1.02)"...
 docList.getListLevels().get(1).setNumberFormat("Section ( .)");
 docList.getListLevels().get(1).setNumberStyle(NumberStyle.LEADING_ZERO);

 // Note that the higher-level uses UppercaseLetter numbering.
 // We can set the "IsLegal" property to use Arabic numbers for the higher list levels.
 docList.getListLevels().get(1).isLegal(true);
 docList.getListLevels().get(1).setRestartAfterLevel(0);

 // Level 3 labels will be upper case Roman numerals with a prefix and a suffix and will restart at each List level 1 item.
 // These list labels will look like "-I-", "-II-"...
 docList.getListLevels().get(2).setNumberFormat("--");
 docList.getListLevels().get(2).setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 docList.getListLevels().get(2).setRestartAfterLevel(1);

 // Make labels of all list levels bold.
 for (ListLevel level : docList.getListLevels())
     level.getFont().setBold(true);

 // Apply list formatting to the current paragraph.
 builder.getListFormat().setList(docList);

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
java.lang.String - The number format for the list level.
### getNumberPosition() {#getNumberPosition}
```
public double getNumberPosition()
```


Gets the position (in points) of the number or bullet for the list level.

 **Remarks:** 

[getNumberPosition()](../../com.aspose.words/listlevel/\#getNumberPosition) / [setNumberPosition(double)](../../com.aspose.words/listlevel/\#setNumberPosition-double) corresponds to LeftIndent plus FirstLineIndent of the paragraph.

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
double - The position (in points) of the number or bullet for the list level.
### getNumberStyle() {#getNumberStyle}
```
public int getNumberStyle()
```


Gets the number style for this list level.

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

Shows advances ways of customizing list labels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 List docList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 // Level 1 labels will be formatted according to the "Heading 1" paragraph style and will have a prefix.
 // These will look like "Appendix A", "Appendix B"...
 docList.getListLevels().get(0).setNumberFormat("Appendix  ");
 docList.getListLevels().get(0).setNumberStyle(NumberStyle.UPPERCASE_LETTER);
 docList.getListLevels().get(0).setLinkedStyle(doc.getStyles().get("Heading 1"));

 // Level 2 labels will display the current numbers of the first and the second list levels and have leading zeroes.
 // If the first list level is at 1, then the list labels from these will look like "Section (1.01)", "Section (1.02)"...
 docList.getListLevels().get(1).setNumberFormat("Section ( .)");
 docList.getListLevels().get(1).setNumberStyle(NumberStyle.LEADING_ZERO);

 // Note that the higher-level uses UppercaseLetter numbering.
 // We can set the "IsLegal" property to use Arabic numbers for the higher list levels.
 docList.getListLevels().get(1).isLegal(true);
 docList.getListLevels().get(1).setRestartAfterLevel(0);

 // Level 3 labels will be upper case Roman numerals with a prefix and a suffix and will restart at each List level 1 item.
 // These list labels will look like "-I-", "-II-"...
 docList.getListLevels().get(2).setNumberFormat("--");
 docList.getListLevels().get(2).setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 docList.getListLevels().get(2).setRestartAfterLevel(1);

 // Make labels of all list levels bold.
 for (ListLevel level : docList.getListLevels())
     level.getFont().setBold(true);

 // Apply list formatting to the current paragraph.
 builder.getListFormat().setList(docList);

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
int - The number style for this list level. The returned value is one of [NumberStyle](../../com.aspose.words/numberstyle/) constants.
### getRestartAfterLevel() {#getRestartAfterLevel}
```
public int getRestartAfterLevel()
```


Gets the list level that must appear before the specified list level restarts numbering.

 **Remarks:** 

The value of -1 means the numbering will continue.

 **Examples:** 

Shows advances ways of customizing list labels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 List docList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 // Level 1 labels will be formatted according to the "Heading 1" paragraph style and will have a prefix.
 // These will look like "Appendix A", "Appendix B"...
 docList.getListLevels().get(0).setNumberFormat("Appendix  ");
 docList.getListLevels().get(0).setNumberStyle(NumberStyle.UPPERCASE_LETTER);
 docList.getListLevels().get(0).setLinkedStyle(doc.getStyles().get("Heading 1"));

 // Level 2 labels will display the current numbers of the first and the second list levels and have leading zeroes.
 // If the first list level is at 1, then the list labels from these will look like "Section (1.01)", "Section (1.02)"...
 docList.getListLevels().get(1).setNumberFormat("Section ( .)");
 docList.getListLevels().get(1).setNumberStyle(NumberStyle.LEADING_ZERO);

 // Note that the higher-level uses UppercaseLetter numbering.
 // We can set the "IsLegal" property to use Arabic numbers for the higher list levels.
 docList.getListLevels().get(1).isLegal(true);
 docList.getListLevels().get(1).setRestartAfterLevel(0);

 // Level 3 labels will be upper case Roman numerals with a prefix and a suffix and will restart at each List level 1 item.
 // These list labels will look like "-I-", "-II-"...
 docList.getListLevels().get(2).setNumberFormat("--");
 docList.getListLevels().get(2).setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 docList.getListLevels().get(2).setRestartAfterLevel(1);

 // Make labels of all list levels bold.
 for (ListLevel level : docList.getListLevels())
     level.getFont().setBold(true);

 // Apply list formatting to the current paragraph.
 builder.getListFormat().setList(docList);

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
int - The list level that must appear before the specified list level restarts numbering.
### getStartAt() {#getStartAt}
```
public int getStartAt()
```


Gets the starting number for this list level.

 **Remarks:** 

Default value is 1.

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
int - The starting number for this list level.
### getTabPosition() {#getTabPosition}
```
public double getTabPosition()
```


Gets the tab position (in points) for the list level.

 **Remarks:** 

Has effect only when [getTrailingCharacter()](../../com.aspose.words/listlevel/\#getTrailingCharacter) / [setTrailingCharacter(int)](../../com.aspose.words/listlevel/\#setTrailingCharacter-int) is a tab.

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
double - The tab position (in points) for the list level.
### getTextPosition() {#getTextPosition}
```
public double getTextPosition()
```


Gets the position (in points) for the second line of wrapping text for the list level.

 **Remarks:** 

[getTextPosition()](../../com.aspose.words/listlevel/\#getTextPosition) / [setTextPosition(double)](../../com.aspose.words/listlevel/\#setTextPosition-double) corresponds to LeftIndent of the paragraph.

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
double - The position (in points) for the second line of wrapping text for the list level.
### getTrailingCharacter() {#getTrailingCharacter}
```
public int getTrailingCharacter()
```


Gets the character inserted after the number for the list level.

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
int - The character inserted after the number for the list level. The returned value is one of [ListTrailingCharacter](../../com.aspose.words/listtrailingcharacter/) constants.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isLegal() {#isLegal}
```
public boolean isLegal()
```


True if the level turns all inherited numbers to Arabic, false if it preserves their number style.

 **Examples:** 

Shows advances ways of customizing list labels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 List docList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 // Level 1 labels will be formatted according to the "Heading 1" paragraph style and will have a prefix.
 // These will look like "Appendix A", "Appendix B"...
 docList.getListLevels().get(0).setNumberFormat("Appendix  ");
 docList.getListLevels().get(0).setNumberStyle(NumberStyle.UPPERCASE_LETTER);
 docList.getListLevels().get(0).setLinkedStyle(doc.getStyles().get("Heading 1"));

 // Level 2 labels will display the current numbers of the first and the second list levels and have leading zeroes.
 // If the first list level is at 1, then the list labels from these will look like "Section (1.01)", "Section (1.02)"...
 docList.getListLevels().get(1).setNumberFormat("Section ( .)");
 docList.getListLevels().get(1).setNumberStyle(NumberStyle.LEADING_ZERO);

 // Note that the higher-level uses UppercaseLetter numbering.
 // We can set the "IsLegal" property to use Arabic numbers for the higher list levels.
 docList.getListLevels().get(1).isLegal(true);
 docList.getListLevels().get(1).setRestartAfterLevel(0);

 // Level 3 labels will be upper case Roman numerals with a prefix and a suffix and will restart at each List level 1 item.
 // These list labels will look like "-I-", "-II-"...
 docList.getListLevels().get(2).setNumberFormat("--");
 docList.getListLevels().get(2).setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 docList.getListLevels().get(2).setRestartAfterLevel(1);

 // Make labels of all list levels bold.
 for (ListLevel level : docList.getListLevels())
     level.getFont().setBold(true);

 // Apply list formatting to the current paragraph.
 builder.getListFormat().setList(docList);

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
boolean - The corresponding  boolean  value.
### isLegal(boolean value) {#isLegal-boolean}
```
public void isLegal(boolean value)
```


True if the level turns all inherited numbers to Arabic, false if it preserves their number style.

 **Examples:** 

Shows advances ways of customizing list labels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 List docList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 // Level 1 labels will be formatted according to the "Heading 1" paragraph style and will have a prefix.
 // These will look like "Appendix A", "Appendix B"...
 docList.getListLevels().get(0).setNumberFormat("Appendix  ");
 docList.getListLevels().get(0).setNumberStyle(NumberStyle.UPPERCASE_LETTER);
 docList.getListLevels().get(0).setLinkedStyle(doc.getStyles().get("Heading 1"));

 // Level 2 labels will display the current numbers of the first and the second list levels and have leading zeroes.
 // If the first list level is at 1, then the list labels from these will look like "Section (1.01)", "Section (1.02)"...
 docList.getListLevels().get(1).setNumberFormat("Section ( .)");
 docList.getListLevels().get(1).setNumberStyle(NumberStyle.LEADING_ZERO);

 // Note that the higher-level uses UppercaseLetter numbering.
 // We can set the "IsLegal" property to use Arabic numbers for the higher list levels.
 docList.getListLevels().get(1).isLegal(true);
 docList.getListLevels().get(1).setRestartAfterLevel(0);

 // Level 3 labels will be upper case Roman numerals with a prefix and a suffix and will restart at each List level 1 item.
 // These list labels will look like "-I-", "-II-"...
 docList.getListLevels().get(2).setNumberFormat("--");
 docList.getListLevels().get(2).setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 docList.getListLevels().get(2).setRestartAfterLevel(1);

 // Make labels of all list levels bold.
 for (ListLevel level : docList.getListLevels())
     level.getFont().setBold(true);

 // Apply list formatting to the current paragraph.
 builder.getListFormat().setList(docList);

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Sets the justification of the actual number of the list item.

 **Remarks:** 

The list label is justified relative to the [getNumberPosition()](../../com.aspose.words/listlevel/\#getNumberPosition) / [setNumberPosition(double)](../../com.aspose.words/listlevel/\#setNumberPosition-double) property.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The justification of the actual number of the list item. The value must be one of [ListLevelAlignment](../../com.aspose.words/listlevelalignment/) constants. |

### setCustomNumberStyleFormat(String value) {#setCustomNumberStyleFormat-java.lang.String}
```
public void setCustomNumberStyleFormat(String value)
```


Sets the custom number style format for this list level. For example: "a, �, \\u011d, ...".

 **Examples:** 

Shows how to get the format for a list with the custom number style.

```

 Document doc = new Document(getMyDir() + "List with leading zero.docx");

 ListLevel listLevel = doc.getFirstSection().getBody().getParagraphs().get(0).getListFormat().getListLevel();

 String customNumberStyleFormat = "";

 if (listLevel.getNumberStyle() == NumberStyle.CUSTOM)
     customNumberStyleFormat = listLevel.getCustomNumberStyleFormat();

 Assert.assertEquals("001, 002, 003, ...", customNumberStyleFormat);

 // We can get value for the specified index of the list item.
 Assert.assertEquals("iv", ListLevel.getEffectiveValue(4, NumberStyle.LOWERCASE_ROMAN, null));
 Assert.assertEquals("005", ListLevel.getEffectiveValue(5, NumberStyle.CUSTOM, customNumberStyleFormat));
 
```

Shows how to set customer number style format.

```

 Document doc = new Document(getMyDir() + "List with leading zero.docx");

 doc.updateListLabels();

 ParagraphCollection paras = doc.getFirstSection().getBody().getParagraphs();
 Assert.assertEquals("001.", paras.get(0).getListLabel().getLabelString());
 Assert.assertEquals("0001.", paras.get(1).getListLabel().getLabelString());
 Assert.assertEquals("0002.", paras.get(2).getListLabel().getLabelString());

 paras.get(1).getListFormat().getListLevel().setCustomNumberStyleFormat("001, 002, 003, ...");

 doc.updateListLabels();

 Assert.assertEquals("001.", paras.get(0).getListLabel().getLabelString());
 Assert.assertEquals("001.", paras.get(1).getListLabel().getLabelString());
 Assert.assertEquals("002.", paras.get(2).getListLabel().getLabelString());
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The custom number style format for this list level. |

### setLinkedStyle(Style value) {#setLinkedStyle-com.aspose.words.Style}
```
public void setLinkedStyle(Style value)
```


Sets the paragraph style that is linked to this list level.

 **Remarks:** 

This property is  null  when the list level is not linked to a paragraph style. This property can be set to  null .

 **Examples:** 

Shows advances ways of customizing list labels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 List docList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 // Level 1 labels will be formatted according to the "Heading 1" paragraph style and will have a prefix.
 // These will look like "Appendix A", "Appendix B"...
 docList.getListLevels().get(0).setNumberFormat("Appendix  ");
 docList.getListLevels().get(0).setNumberStyle(NumberStyle.UPPERCASE_LETTER);
 docList.getListLevels().get(0).setLinkedStyle(doc.getStyles().get("Heading 1"));

 // Level 2 labels will display the current numbers of the first and the second list levels and have leading zeroes.
 // If the first list level is at 1, then the list labels from these will look like "Section (1.01)", "Section (1.02)"...
 docList.getListLevels().get(1).setNumberFormat("Section ( .)");
 docList.getListLevels().get(1).setNumberStyle(NumberStyle.LEADING_ZERO);

 // Note that the higher-level uses UppercaseLetter numbering.
 // We can set the "IsLegal" property to use Arabic numbers for the higher list levels.
 docList.getListLevels().get(1).isLegal(true);
 docList.getListLevels().get(1).setRestartAfterLevel(0);

 // Level 3 labels will be upper case Roman numerals with a prefix and a suffix and will restart at each List level 1 item.
 // These list labels will look like "-I-", "-II-"...
 docList.getListLevels().get(2).setNumberFormat("--");
 docList.getListLevels().get(2).setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 docList.getListLevels().get(2).setRestartAfterLevel(1);

 // Make labels of all list levels bold.
 for (ListLevel level : docList.getListLevels())
     level.getFont().setBold(true);

 // Apply list formatting to the current paragraph.
 builder.getListFormat().setList(docList);

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style/) | The paragraph style that is linked to this list level. |

### setNumberFormat(String value) {#setNumberFormat-java.lang.String}
```
public void setNumberFormat(String value)
```


Sets the number format for the list level.

 **Remarks:** 

Among normal text characters, the string can contain placeholder characters \\x0000 to \\x0008 representing the numbers from the corresponding list levels.

For example, the string "\\x0000.\\x0001)" will generate a list label that looks something like "1.5)". The number "1" is the current number from the 1st list level, the number "5" is the current number from the 2nd list level.

Null is not allowed, but an empty string meaning no number is valid.

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

Shows advances ways of customizing list labels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 List docList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 // Level 1 labels will be formatted according to the "Heading 1" paragraph style and will have a prefix.
 // These will look like "Appendix A", "Appendix B"...
 docList.getListLevels().get(0).setNumberFormat("Appendix  ");
 docList.getListLevels().get(0).setNumberStyle(NumberStyle.UPPERCASE_LETTER);
 docList.getListLevels().get(0).setLinkedStyle(doc.getStyles().get("Heading 1"));

 // Level 2 labels will display the current numbers of the first and the second list levels and have leading zeroes.
 // If the first list level is at 1, then the list labels from these will look like "Section (1.01)", "Section (1.02)"...
 docList.getListLevels().get(1).setNumberFormat("Section ( .)");
 docList.getListLevels().get(1).setNumberStyle(NumberStyle.LEADING_ZERO);

 // Note that the higher-level uses UppercaseLetter numbering.
 // We can set the "IsLegal" property to use Arabic numbers for the higher list levels.
 docList.getListLevels().get(1).isLegal(true);
 docList.getListLevels().get(1).setRestartAfterLevel(0);

 // Level 3 labels will be upper case Roman numerals with a prefix and a suffix and will restart at each List level 1 item.
 // These list labels will look like "-I-", "-II-"...
 docList.getListLevels().get(2).setNumberFormat("--");
 docList.getListLevels().get(2).setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 docList.getListLevels().get(2).setRestartAfterLevel(1);

 // Make labels of all list levels bold.
 for (ListLevel level : docList.getListLevels())
     level.getFont().setBold(true);

 // Apply list formatting to the current paragraph.
 builder.getListFormat().setList(docList);

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The number format for the list level. |

### setNumberPosition(double value) {#setNumberPosition-double}
```
public void setNumberPosition(double value)
```


Sets the position (in points) of the number or bullet for the list level.

 **Remarks:** 

[getNumberPosition()](../../com.aspose.words/listlevel/\#getNumberPosition) / [setNumberPosition(double)](../../com.aspose.words/listlevel/\#setNumberPosition-double) corresponds to LeftIndent plus FirstLineIndent of the paragraph.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The position (in points) of the number or bullet for the list level. |

### setNumberStyle(int value) {#setNumberStyle-int}
```
public void setNumberStyle(int value)
```


Sets the number style for this list level.

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

Shows advances ways of customizing list labels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 List docList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 // Level 1 labels will be formatted according to the "Heading 1" paragraph style and will have a prefix.
 // These will look like "Appendix A", "Appendix B"...
 docList.getListLevels().get(0).setNumberFormat("Appendix  ");
 docList.getListLevels().get(0).setNumberStyle(NumberStyle.UPPERCASE_LETTER);
 docList.getListLevels().get(0).setLinkedStyle(doc.getStyles().get("Heading 1"));

 // Level 2 labels will display the current numbers of the first and the second list levels and have leading zeroes.
 // If the first list level is at 1, then the list labels from these will look like "Section (1.01)", "Section (1.02)"...
 docList.getListLevels().get(1).setNumberFormat("Section ( .)");
 docList.getListLevels().get(1).setNumberStyle(NumberStyle.LEADING_ZERO);

 // Note that the higher-level uses UppercaseLetter numbering.
 // We can set the "IsLegal" property to use Arabic numbers for the higher list levels.
 docList.getListLevels().get(1).isLegal(true);
 docList.getListLevels().get(1).setRestartAfterLevel(0);

 // Level 3 labels will be upper case Roman numerals with a prefix and a suffix and will restart at each List level 1 item.
 // These list labels will look like "-I-", "-II-"...
 docList.getListLevels().get(2).setNumberFormat("--");
 docList.getListLevels().get(2).setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 docList.getListLevels().get(2).setRestartAfterLevel(1);

 // Make labels of all list levels bold.
 for (ListLevel level : docList.getListLevels())
     level.getFont().setBold(true);

 // Apply list formatting to the current paragraph.
 builder.getListFormat().setList(docList);

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The number style for this list level. The value must be one of [NumberStyle](../../com.aspose.words/numberstyle/) constants. |

### setRestartAfterLevel(int value) {#setRestartAfterLevel-int}
```
public void setRestartAfterLevel(int value)
```


Sets the list level that must appear before the specified list level restarts numbering.

 **Remarks:** 

The value of -1 means the numbering will continue.

 **Examples:** 

Shows advances ways of customizing list labels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 List docList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 // Level 1 labels will be formatted according to the "Heading 1" paragraph style and will have a prefix.
 // These will look like "Appendix A", "Appendix B"...
 docList.getListLevels().get(0).setNumberFormat("Appendix  ");
 docList.getListLevels().get(0).setNumberStyle(NumberStyle.UPPERCASE_LETTER);
 docList.getListLevels().get(0).setLinkedStyle(doc.getStyles().get("Heading 1"));

 // Level 2 labels will display the current numbers of the first and the second list levels and have leading zeroes.
 // If the first list level is at 1, then the list labels from these will look like "Section (1.01)", "Section (1.02)"...
 docList.getListLevels().get(1).setNumberFormat("Section ( .)");
 docList.getListLevels().get(1).setNumberStyle(NumberStyle.LEADING_ZERO);

 // Note that the higher-level uses UppercaseLetter numbering.
 // We can set the "IsLegal" property to use Arabic numbers for the higher list levels.
 docList.getListLevels().get(1).isLegal(true);
 docList.getListLevels().get(1).setRestartAfterLevel(0);

 // Level 3 labels will be upper case Roman numerals with a prefix and a suffix and will restart at each List level 1 item.
 // These list labels will look like "-I-", "-II-"...
 docList.getListLevels().get(2).setNumberFormat("--");
 docList.getListLevels().get(2).setNumberStyle(NumberStyle.UPPERCASE_ROMAN);
 docList.getListLevels().get(2).setRestartAfterLevel(1);

 // Make labels of all list levels bold.
 for (ListLevel level : docList.getListLevels())
     level.getFont().setBold(true);

 // Apply list formatting to the current paragraph.
 builder.getListFormat().setList(docList);

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The list level that must appear before the specified list level restarts numbering. |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setStartAt(int value) {#setStartAt-int}
```
public void setStartAt(int value)
```


Sets the starting number for this list level.

 **Remarks:** 

Default value is 1.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The starting number for this list level. |

### setTabPosition(double value) {#setTabPosition-double}
```
public void setTabPosition(double value)
```


Sets the tab position (in points) for the list level.

 **Remarks:** 

Has effect only when [getTrailingCharacter()](../../com.aspose.words/listlevel/\#getTrailingCharacter) / [setTrailingCharacter(int)](../../com.aspose.words/listlevel/\#setTrailingCharacter-int) is a tab.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The tab position (in points) for the list level. |

### setTextPosition(double value) {#setTextPosition-double}
```
public void setTextPosition(double value)
```


Sets the position (in points) for the second line of wrapping text for the list level.

 **Remarks:** 

[getTextPosition()](../../com.aspose.words/listlevel/\#getTextPosition) / [setTextPosition(double)](../../com.aspose.words/listlevel/\#setTextPosition-double) corresponds to LeftIndent of the paragraph.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The position (in points) for the second line of wrapping text for the list level. |

### setTrailingCharacter(int value) {#setTrailingCharacter-int}
```
public void setTrailingCharacter(int value)
```


Sets the character inserted after the number for the list level.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The character inserted after the number for the list level. The value must be one of [ListTrailingCharacter](../../com.aspose.words/listtrailingcharacter/) constants. |

