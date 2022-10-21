---
title: ListLevel
second_title: Aspose.Words for Java API Reference
description: Defines formatting for a list level.
type: docs
weight: 372
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

To learn more, visit the **Working with Lists** documentation article.

You do not create objects of this class. List level objects are created automatically when a list is created. You access [ListLevel](../../com.aspose.words/listlevel) objects via the [ListLevelCollection](../../com.aspose.words/listlevelcollection) collection.

Use the properties of [ListLevel](../../com.aspose.words/listlevel) to specify list formatting for individual list levels.
## Methods

| Method | Description |
| --- | --- |
| [createPictureBullet()](#createPictureBullet--) | Creates picture bullet shape for the current list level. |
| [deletePictureBullet()](#deletePictureBullet--) | Deletes picture bullet for the current list level. |
| [getEffectiveValue(int index, int numberStyle, String customNumberStyleFormat)](#getEffectiveValue-int-int-java.lang.String-) |  |
| [equals(ListLevel level)](#equals-com.aspose.words.ListLevel-) | Compares with the specified ListLevel. |
| [hashCode()](#hashCode--) |  |
| [getStartAt()](#getStartAt--) | Gets the starting number for this list level. |
| [setStartAt(int value)](#setStartAt-int-) | Sets the starting number for this list level. |
| [getNumberStyle()](#getNumberStyle--) | Gets the number style for this list level. |
| [setNumberStyle(int value)](#setNumberStyle-int-) | Sets the number style for this list level. |
| [getCustomNumberStyleFormat()](#getCustomNumberStyleFormat--) | Gets the custom number style format for this list level. |
| [getNumberFormat()](#getNumberFormat--) | Gets the number format for the list level. |
| [setNumberFormat(String value)](#setNumberFormat-java.lang.String-) | Sets the number format for the list level. |
| [getAlignment()](#getAlignment--) | Gets the justification of the actual number of the list item. |
| [setAlignment(int value)](#setAlignment-int-) | Sets the justification of the actual number of the list item. |
| [isLegal()](#isLegal--) | True if the level turns all inherited numbers to Arabic, false if it preserves their number style. |
| [isLegal(boolean value)](#isLegal-boolean-) | True if the level turns all inherited numbers to Arabic, false if it preserves their number style. |
| [getRestartAfterLevel()](#getRestartAfterLevel--) | Gets the list level that must appear before the specified list level restarts numbering. |
| [setRestartAfterLevel(int value)](#setRestartAfterLevel-int-) | Sets the list level that must appear before the specified list level restarts numbering. |
| [getTrailingCharacter()](#getTrailingCharacter--) | Gets the character inserted after the number for the list level. |
| [setTrailingCharacter(int value)](#setTrailingCharacter-int-) | Sets the character inserted after the number for the list level. |
| [getFont()](#getFont--) | Specifies character formatting used for the list label. |
| [getTabPosition()](#getTabPosition--) | Gets the tab position (in points) for the list level. |
| [setTabPosition(double value)](#setTabPosition-double-) | Sets the tab position (in points) for the list level. |
| [getNumberPosition()](#getNumberPosition--) | Gets the position (in points) of the number or bullet for the list level. |
| [setNumberPosition(double value)](#setNumberPosition-double-) | Sets the position (in points) of the number or bullet for the list level. |
| [getTextPosition()](#getTextPosition--) | Gets the position (in points) for the second line of wrapping text for the list level. |
| [setTextPosition(double value)](#setTextPosition-double-) | Sets the position (in points) for the second line of wrapping text for the list level. |
| [getLinkedStyle()](#getLinkedStyle--) | Gets the paragraph style that is linked to this list level. |
| [setLinkedStyle(Style value)](#setLinkedStyle-com.aspose.words.Style-) | Sets the paragraph style that is linked to this list level. |
| [getImageData()](#getImageData--) | Returns image data of the picture bullet shape for the current list level. |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
### createPictureBullet() {#createPictureBullet--}
```
public void createPictureBullet()
```


Creates picture bullet shape for the current list level. Please note, NumberStyle will be set to Bullet and NumberFormat to "\\xF0B7" to properly display picture bullet. Red cross image will be set as picture bullet image upon creating. To change it please use [getImageData()](../../com.aspose.words/listlevel\#getImageData--).

### deletePictureBullet() {#deletePictureBullet--}
```
public void deletePictureBullet()
```


Deletes picture bullet for the current list level. Default bullet will be shown after deleting.

### getEffectiveValue(int index, int numberStyle, String customNumberStyleFormat) {#getEffectiveValue-int-int-java.lang.String-}
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
### equals(ListLevel level) {#equals-com.aspose.words.ListLevel-}
```
public boolean equals(ListLevel level)
```


Compares with the specified ListLevel.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| level | [ListLevel](../../com.aspose.words/listlevel) |  |

**Returns:**
boolean
### hashCode() {#hashCode--}
```
public int hashCode()
```




**Returns:**
int
### getStartAt() {#getStartAt--}
```
public int getStartAt()
```


Gets the starting number for this list level.

Default value is 1.

**Returns:**
int - The starting number for this list level.
### setStartAt(int value) {#setStartAt-int-}
```
public void setStartAt(int value)
```


Sets the starting number for this list level.

Default value is 1.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The starting number for this list level. |

### getNumberStyle() {#getNumberStyle--}
```
public int getNumberStyle()
```


Gets the number style for this list level.

**Returns:**
int - The number style for this list level. The returned value is one of [NumberStyle](../../com.aspose.words/numberstyle) constants.
### setNumberStyle(int value) {#setNumberStyle-int-}
```
public void setNumberStyle(int value)
```


Sets the number style for this list level.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The number style for this list level. The value must be one of [NumberStyle](../../com.aspose.words/numberstyle) constants. |

### getCustomNumberStyleFormat() {#getCustomNumberStyleFormat--}
```
public String getCustomNumberStyleFormat()
```


Gets the custom number style format for this list level. For example: "a, ç, \\u011d, ...".

**Returns:**
java.lang.String - The custom number style format for this list level.
### getNumberFormat() {#getNumberFormat--}
```
public String getNumberFormat()
```


Gets the number format for the list level.

Among normal text characters, the string can contain placeholder characters \\x0000 to \\x0008 representing the numbers from the corresponding list levels.

For example, the string "\\x0000.\\x0001)" will generate a list label that looks something like "1.5)". The number "1" is the current number from the 1st list level, the number "5" is the current number from the 2nd list level.

Null is not allowed, but an empty string meaning no number is valid.

**Returns:**
java.lang.String - The number format for the list level.
### setNumberFormat(String value) {#setNumberFormat-java.lang.String-}
```
public void setNumberFormat(String value)
```


Sets the number format for the list level.

Among normal text characters, the string can contain placeholder characters \\x0000 to \\x0008 representing the numbers from the corresponding list levels.

For example, the string "\\x0000.\\x0001)" will generate a list label that looks something like "1.5)". The number "1" is the current number from the 1st list level, the number "5" is the current number from the 2nd list level.

Null is not allowed, but an empty string meaning no number is valid.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The number format for the list level. |

### getAlignment() {#getAlignment--}
```
public int getAlignment()
```


Gets the justification of the actual number of the list item.

The list label is justified relative to the [getNumberPosition()](../../com.aspose.words/listlevel\#getNumberPosition--) / [setNumberPosition(double)](../../com.aspose.words/listlevel\#setNumberPosition-double-) property.

**Returns:**
int - The justification of the actual number of the list item. The returned value is one of [ListLevelAlignment](../../com.aspose.words/listlevelalignment) constants.
### setAlignment(int value) {#setAlignment-int-}
```
public void setAlignment(int value)
```


Sets the justification of the actual number of the list item.

The list label is justified relative to the [getNumberPosition()](../../com.aspose.words/listlevel\#getNumberPosition--) / [setNumberPosition(double)](../../com.aspose.words/listlevel\#setNumberPosition-double-) property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The justification of the actual number of the list item. The value must be one of [ListLevelAlignment](../../com.aspose.words/listlevelalignment) constants. |

### isLegal() {#isLegal--}
```
public boolean isLegal()
```


True if the level turns all inherited numbers to Arabic, false if it preserves their number style.

**Returns:**
boolean - The corresponding  boolean  value.
### isLegal(boolean value) {#isLegal-boolean-}
```
public void isLegal(boolean value)
```


True if the level turns all inherited numbers to Arabic, false if it preserves their number style.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getRestartAfterLevel() {#getRestartAfterLevel--}
```
public int getRestartAfterLevel()
```


Gets the list level that must appear before the specified list level restarts numbering.

The value of -1 means the numbering will continue.

**Returns:**
int - The list level that must appear before the specified list level restarts numbering.
### setRestartAfterLevel(int value) {#setRestartAfterLevel-int-}
```
public void setRestartAfterLevel(int value)
```


Sets the list level that must appear before the specified list level restarts numbering.

The value of -1 means the numbering will continue.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The list level that must appear before the specified list level restarts numbering. |

### getTrailingCharacter() {#getTrailingCharacter--}
```
public int getTrailingCharacter()
```


Gets the character inserted after the number for the list level.

**Returns:**
int - The character inserted after the number for the list level. The returned value is one of [ListTrailingCharacter](../../com.aspose.words/listtrailingcharacter) constants.
### setTrailingCharacter(int value) {#setTrailingCharacter-int-}
```
public void setTrailingCharacter(int value)
```


Sets the character inserted after the number for the list level.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The character inserted after the number for the list level. The value must be one of [ListTrailingCharacter](../../com.aspose.words/listtrailingcharacter) constants. |

### getFont() {#getFont--}
```
public Font getFont()
```


Specifies character formatting used for the list label.

**Returns:**
[Font](../../com.aspose.words/font) - The corresponding [Font](../../com.aspose.words/font) value.
### getTabPosition() {#getTabPosition--}
```
public double getTabPosition()
```


Gets the tab position (in points) for the list level.

Has effect only when [getTrailingCharacter()](../../com.aspose.words/listlevel\#getTrailingCharacter--) / [setTrailingCharacter(int)](../../com.aspose.words/listlevel\#setTrailingCharacter-int-) is a tab.

**Returns:**
double - The tab position (in points) for the list level.
### setTabPosition(double value) {#setTabPosition-double-}
```
public void setTabPosition(double value)
```


Sets the tab position (in points) for the list level.

Has effect only when [getTrailingCharacter()](../../com.aspose.words/listlevel\#getTrailingCharacter--) / [setTrailingCharacter(int)](../../com.aspose.words/listlevel\#setTrailingCharacter-int-) is a tab.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The tab position (in points) for the list level. |

### getNumberPosition() {#getNumberPosition--}
```
public double getNumberPosition()
```


Gets the position (in points) of the number or bullet for the list level.

[getNumberPosition()](../../com.aspose.words/listlevel\#getNumberPosition--) / [setNumberPosition(double)](../../com.aspose.words/listlevel\#setNumberPosition-double-) corresponds to LeftIndent plus FirstLineIndent of the paragraph.

**Returns:**
double - The position (in points) of the number or bullet for the list level.
### setNumberPosition(double value) {#setNumberPosition-double-}
```
public void setNumberPosition(double value)
```


Sets the position (in points) of the number or bullet for the list level.

[getNumberPosition()](../../com.aspose.words/listlevel\#getNumberPosition--) / [setNumberPosition(double)](../../com.aspose.words/listlevel\#setNumberPosition-double-) corresponds to LeftIndent plus FirstLineIndent of the paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The position (in points) of the number or bullet for the list level. |

### getTextPosition() {#getTextPosition--}
```
public double getTextPosition()
```


Gets the position (in points) for the second line of wrapping text for the list level.

[getTextPosition()](../../com.aspose.words/listlevel\#getTextPosition--) / [setTextPosition(double)](../../com.aspose.words/listlevel\#setTextPosition-double-) corresponds to LeftIndent of the paragraph.

**Returns:**
double - The position (in points) for the second line of wrapping text for the list level.
### setTextPosition(double value) {#setTextPosition-double-}
```
public void setTextPosition(double value)
```


Sets the position (in points) for the second line of wrapping text for the list level.

[getTextPosition()](../../com.aspose.words/listlevel\#getTextPosition--) / [setTextPosition(double)](../../com.aspose.words/listlevel\#setTextPosition-double-) corresponds to LeftIndent of the paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The position (in points) for the second line of wrapping text for the list level. |

### getLinkedStyle() {#getLinkedStyle--}
```
public Style getLinkedStyle()
```


Gets the paragraph style that is linked to this list level.

This property is null when the list level is not linked to a paragraph style. This property can be set to null.

**Returns:**
[Style](../../com.aspose.words/style) - The paragraph style that is linked to this list level.
### setLinkedStyle(Style value) {#setLinkedStyle-com.aspose.words.Style-}
```
public void setLinkedStyle(Style value)
```


Sets the paragraph style that is linked to this list level.

This property is null when the list level is not linked to a paragraph style. This property can be set to null.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style) | The paragraph style that is linked to this list level. |

### getImageData() {#getImageData--}
```
public ImageData getImageData()
```


Returns image data of the picture bullet shape for the current list level. If this level doesn't define picture bullet returns null. Before setting new image for non picture bullet shape, please use [createPictureBullet()](../../com.aspose.words/listlevel\#createPictureBullet--) method first.

**Returns:**
[ImageData](../../com.aspose.words/imagedata) - Image data of the picture bullet shape for the current list level.
### getDirectRunAttr(int key) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




