---
title: ListLevel
second_title: Aspose.Words for Java API Reference
description: Defines formatting for a list level.
type: docs
weight: 374
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

You do not create objects of this class. List level objects are created automatically when a list is created. You access [ListLevel](../../com.aspose.words/listlevel) objects via the [ListLevelCollection](../../com.aspose.words/listlevelcollection) collection.

Use the properties of [ListLevel](../../com.aspose.words/listlevel) to specify list formatting for individual list levels.


[Working with Lists]: https://docs.aspose.com/words/java/working-with-lists/
## Methods

| Method | Description |
| --- | --- |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [createPictureBullet()](#createPictureBullet) | Creates picture bullet shape for the current list level. |
| [deletePictureBullet()](#deletePictureBullet) | Deletes picture bullet for the current list level. |
| [equals(ListLevel level)](#equals-com.aspose.words.ListLevel) | Compares with the specified ListLevel. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [getAlignment()](#getAlignment) | Gets the justification of the actual number of the list item. |
| [getClass()](#getClass) |  |
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
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [setAlignment(int value)](#setAlignment-int) | Sets the justification of the actual number of the list item. |
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
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### createPictureBullet() {#createPictureBullet}
```
public void createPictureBullet()
```


Creates picture bullet shape for the current list level. Please note, [getNumberStyle()](../../com.aspose.words/listlevel\#getNumberStyle) / [setNumberStyle(int)](../../com.aspose.words/listlevel\#setNumberStyle-int) will be set to [NumberStyle.BULLET](../../com.aspose.words/numberstyle\#BULLET) and [getNumberFormat()](../../com.aspose.words/listlevel\#getNumberFormat) / [setNumberFormat(java.lang.String)](../../com.aspose.words/listlevel\#setNumberFormat-java.lang.String) to "\\xF0B7" to properly display picture bullet. Red cross image will be set as picture bullet image upon creating. To change it please use [getImageData()](../../com.aspose.words/listlevel\#getImageData).

### deletePictureBullet() {#deletePictureBullet}
```
public void deletePictureBullet()
```


Deletes picture bullet for the current list level. Default bullet will be shown after deleting.

### equals(ListLevel level) {#equals-com.aspose.words.ListLevel}
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
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

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

The list label is justified relative to the [getNumberPosition()](../../com.aspose.words/listlevel\#getNumberPosition) / [setNumberPosition(double)](../../com.aspose.words/listlevel\#setNumberPosition-double) property.

**Returns:**
int - The justification of the actual number of the list item. The returned value is one of [ListLevelAlignment](../../com.aspose.words/listlevelalignment) constants.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCustomNumberStyleFormat() {#getCustomNumberStyleFormat}
```
public String getCustomNumberStyleFormat()
```


Gets the custom number style format for this list level. For example: "a, ç, \\u011d, ...".

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

**Returns:**
[Font](../../com.aspose.words/font) - The corresponding [Font](../../com.aspose.words/font) value.
### getImageData() {#getImageData}
```
public ImageData getImageData()
```


Returns image data of the picture bullet shape for the current list level. If this level doesn't define picture bullet returns  null . Before setting new image for non picture bullet shape, please use [createPictureBullet()](../../com.aspose.words/listlevel\#createPictureBullet) method first.

**Returns:**
[ImageData](../../com.aspose.words/imagedata) - Image data of the picture bullet shape for the current list level.
### getLinkedStyle() {#getLinkedStyle}
```
public Style getLinkedStyle()
```


Gets the paragraph style that is linked to this list level.

This property is  null  when the list level is not linked to a paragraph style. This property can be set to  null .

**Returns:**
[Style](../../com.aspose.words/style) - The paragraph style that is linked to this list level.
### getNumberFormat() {#getNumberFormat}
```
public String getNumberFormat()
```


Gets the number format for the list level.

Among normal text characters, the string can contain placeholder characters \\x0000 to \\x0008 representing the numbers from the corresponding list levels.

For example, the string "\\x0000.\\x0001)" will generate a list label that looks something like "1.5)". The number "1" is the current number from the 1st list level, the number "5" is the current number from the 2nd list level.

Null is not allowed, but an empty string meaning no number is valid.

**Returns:**
java.lang.String - The number format for the list level.
### getNumberPosition() {#getNumberPosition}
```
public double getNumberPosition()
```


Gets the position (in points) of the number or bullet for the list level.

[getNumberPosition()](../../com.aspose.words/listlevel\#getNumberPosition) / [setNumberPosition(double)](../../com.aspose.words/listlevel\#setNumberPosition-double) corresponds to LeftIndent plus FirstLineIndent of the paragraph.

**Returns:**
double - The position (in points) of the number or bullet for the list level.
### getNumberStyle() {#getNumberStyle}
```
public int getNumberStyle()
```


Gets the number style for this list level.

**Returns:**
int - The number style for this list level. The returned value is one of [NumberStyle](../../com.aspose.words/numberstyle) constants.
### getRestartAfterLevel() {#getRestartAfterLevel}
```
public int getRestartAfterLevel()
```


Gets the list level that must appear before the specified list level restarts numbering.

The value of -1 means the numbering will continue.

**Returns:**
int - The list level that must appear before the specified list level restarts numbering.
### getStartAt() {#getStartAt}
```
public int getStartAt()
```


Gets the starting number for this list level.

Default value is 1.

**Returns:**
int - The starting number for this list level.
### getTabPosition() {#getTabPosition}
```
public double getTabPosition()
```


Gets the tab position (in points) for the list level.

Has effect only when [getTrailingCharacter()](../../com.aspose.words/listlevel\#getTrailingCharacter) / [setTrailingCharacter(int)](../../com.aspose.words/listlevel\#setTrailingCharacter-int) is a tab.

**Returns:**
double - The tab position (in points) for the list level.
### getTextPosition() {#getTextPosition}
```
public double getTextPosition()
```


Gets the position (in points) for the second line of wrapping text for the list level.

[getTextPosition()](../../com.aspose.words/listlevel\#getTextPosition) / [setTextPosition(double)](../../com.aspose.words/listlevel\#setTextPosition-double) corresponds to LeftIndent of the paragraph.

**Returns:**
double - The position (in points) for the second line of wrapping text for the list level.
### getTrailingCharacter() {#getTrailingCharacter}
```
public int getTrailingCharacter()
```


Gets the character inserted after the number for the list level.

**Returns:**
int - The character inserted after the number for the list level. The returned value is one of [ListTrailingCharacter](../../com.aspose.words/listtrailingcharacter) constants.
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

**Returns:**
boolean - The corresponding  boolean  value.
### isLegal(boolean value) {#isLegal-boolean}
```
public void isLegal(boolean value)
```


True if the level turns all inherited numbers to Arabic, false if it preserves their number style.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




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

The list label is justified relative to the [getNumberPosition()](../../com.aspose.words/listlevel\#getNumberPosition) / [setNumberPosition(double)](../../com.aspose.words/listlevel\#setNumberPosition-double) property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The justification of the actual number of the list item. The value must be one of [ListLevelAlignment](../../com.aspose.words/listlevelalignment) constants. |

### setLinkedStyle(Style value) {#setLinkedStyle-com.aspose.words.Style}
```
public void setLinkedStyle(Style value)
```


Sets the paragraph style that is linked to this list level.

This property is  null  when the list level is not linked to a paragraph style. This property can be set to  null .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style) | The paragraph style that is linked to this list level. |

### setNumberFormat(String value) {#setNumberFormat-java.lang.String}
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

### setNumberPosition(double value) {#setNumberPosition-double}
```
public void setNumberPosition(double value)
```


Sets the position (in points) of the number or bullet for the list level.

[getNumberPosition()](../../com.aspose.words/listlevel\#getNumberPosition) / [setNumberPosition(double)](../../com.aspose.words/listlevel\#setNumberPosition-double) corresponds to LeftIndent plus FirstLineIndent of the paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The position (in points) of the number or bullet for the list level. |

### setNumberStyle(int value) {#setNumberStyle-int}
```
public void setNumberStyle(int value)
```


Sets the number style for this list level.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The number style for this list level. The value must be one of [NumberStyle](../../com.aspose.words/numberstyle) constants. |

### setRestartAfterLevel(int value) {#setRestartAfterLevel-int}
```
public void setRestartAfterLevel(int value)
```


Sets the list level that must appear before the specified list level restarts numbering.

The value of -1 means the numbering will continue.

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

Default value is 1.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The starting number for this list level. |

### setTabPosition(double value) {#setTabPosition-double}
```
public void setTabPosition(double value)
```


Sets the tab position (in points) for the list level.

Has effect only when [getTrailingCharacter()](../../com.aspose.words/listlevel\#getTrailingCharacter) / [setTrailingCharacter(int)](../../com.aspose.words/listlevel\#setTrailingCharacter-int) is a tab.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The tab position (in points) for the list level. |

### setTextPosition(double value) {#setTextPosition-double}
```
public void setTextPosition(double value)
```


Sets the position (in points) for the second line of wrapping text for the list level.

[getTextPosition()](../../com.aspose.words/listlevel\#getTextPosition) / [setTextPosition(double)](../../com.aspose.words/listlevel\#setTextPosition-double) corresponds to LeftIndent of the paragraph.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The position (in points) for the second line of wrapping text for the list level. |

### setTrailingCharacter(int value) {#setTrailingCharacter-int}
```
public void setTrailingCharacter(int value)
```


Sets the character inserted after the number for the list level.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The character inserted after the number for the list level. The value must be one of [ListTrailingCharacter](../../com.aspose.words/listtrailingcharacter) constants. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

