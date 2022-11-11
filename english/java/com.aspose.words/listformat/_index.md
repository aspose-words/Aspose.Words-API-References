---
title: ListFormat
second_title: Aspose.Words for Java API Reference
description: Allows to control what list formatting is applied to a paragraph.
type: docs
weight: 370
url: /java/com.aspose.words/listformat/
---

**Inheritance:**
java.lang.Object
```
public class ListFormat
```

Allows to control what list formatting is applied to a paragraph.

To learn more, visit the **Working with Lists** documentation article.

A paragraph in a Microsoft Word document can be bulleted or numbered. When a paragraph is bulleted or numbered, it is said that list formatting is applied to the paragraph.

You do not create objects of the [ListFormat](../../com.aspose.words/listformat) class directly. You access [ListFormat](../../com.aspose.words/listformat) as a property of another object that can have list formatting associated with it. At the moment the objects that can have list formatting are: [Paragraph](../../com.aspose.words/paragraph), [Style](../../com.aspose.words/style) and [DocumentBuilder](../../com.aspose.words/documentbuilder).

[ListFormat](../../com.aspose.words/listformat) of a [Paragraph](../../com.aspose.words/paragraph) specifies what list formatting and list level is applied to that particular paragraph.

[ListFormat](../../com.aspose.words/listformat) of a [Style](../../com.aspose.words/style) (applicable to paragraph styles only) allows to specify what list formatting and list level is applied to all paragraphs of that particular style.

[ListFormat](../../com.aspose.words/listformat) of a [DocumentBuilder](../../com.aspose.words/documentbuilder) provides access to the list formatting at the current cursor position inside the [DocumentBuilder](../../com.aspose.words/documentbuilder).

The list formatting itself is stored inside a [List](../../com.aspose.words/list) object that is stored separately from the paragraphs. The list objects are stored inside a [ListCollection](../../com.aspose.words/listcollection) collection. There is a single [ListCollection](../../com.aspose.words/listcollection) collection per [Document](../../com.aspose.words/document).

The paragraphs do not physically belong to a list. The paragraphs just reference a particular list object via the [getList()](../../com.aspose.words/listformat\#getList--) / [setList(com.aspose.words.List)](../../com.aspose.words/listformat\#setList-com.aspose.words.List-) property and a particular level in the list via the [getListLevelNumber()](../../com.aspose.words/listformat\#getListLevelNumber--) / [setListLevelNumber(int)](../../com.aspose.words/listformat\#setListLevelNumber-int-) property. By setting these two properties you control what bullets and numbering is applied to a paragraph.
## Methods

| Method | Description |
| --- | --- |
| [applyBulletDefault()](#applyBulletDefault--) | Starts a new default bulleted list and applies it to the paragraph. |
| [applyNumberDefault()](#applyNumberDefault--) | Starts a new default numbered list and applies it to the paragraph. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getList()](#getList--) | Gets the list this paragraph is a member of. |
| [getListLevel()](#getListLevel--) | Returns the list level formatting plus any formatting overrides applied to the current paragraph. |
| [getListLevelNumber()](#getListLevelNumber--) | Gets the list level number (0 to 8) for the paragraph. |
| [hashCode()](#hashCode--) |  |
| [isListItem()](#isListItem--) | True when the paragraph has bulleted or numbered formatting applied to it. |
| [listIndent()](#listIndent--) | Increases the list level of the current paragraph by one level. |
| [listOutdent()](#listOutdent--) | Decreases the list level of the current paragraph by one level. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeNumbers()](#removeNumbers--) | Removes numbers or bullets from the current paragraph and sets list level to zero. |
| [setList(List value)](#setList-com.aspose.words.List-) | Sets the list this paragraph is a member of. |
| [setListLevelNumber(int value)](#setListLevelNumber-int-) | Sets the list level number (0 to 8) for the paragraph. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### applyBulletDefault() {#applyBulletDefault--}
```
public void applyBulletDefault()
```


Starts a new default bulleted list and applies it to the paragraph.

This is a shortcut method that creates a new list using the default bulleted template, applies it to the paragraph and selects the 1st list level.

### applyNumberDefault() {#applyNumberDefault--}
```
public void applyNumberDefault()
```


Starts a new default numbered list and applies it to the paragraph.

This is a shortcut method that creates a new list using the default numbered template, applies it to the paragraph and selects the 1st list level.

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getList() {#getList--}
```
public List getList()
```


Gets the list this paragraph is a member of.

The list that is being assigned to this property must belong to the current document.

The list that is being assigned to this property must not be a list style definition.

Setting this property to null removes bullets and numbering from the paragraph and sets the list level number to zero. Setting this property to null is equivalent to calling [removeNumbers()](../../com.aspose.words/listformat\#removeNumbers--).

**Returns:**
[List](../../com.aspose.words/list) - The list this paragraph is a member of.
### getListLevel() {#getListLevel--}
```
public ListLevel getListLevel()
```


Returns the list level formatting plus any formatting overrides applied to the current paragraph.

**Returns:**
[ListLevel](../../com.aspose.words/listlevel) - The list level formatting plus any formatting overrides applied to the current paragraph.
### getListLevelNumber() {#getListLevelNumber--}
```
public int getListLevelNumber()
```


Gets the list level number (0 to 8) for the paragraph.

In Word documents, lists may consist of 1 or 9 levels, numbered 0 to 8.

Has effect only when the [getList()](../../com.aspose.words/listformat\#getList--) / [setList(com.aspose.words.List)](../../com.aspose.words/listformat\#setList-com.aspose.words.List-) property is set to reference a valid list.

**Returns:**
int - The list level number (0 to 8) for the paragraph.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### isListItem() {#isListItem--}
```
public boolean isListItem()
```


True when the paragraph has bulleted or numbered formatting applied to it.

**Returns:**
boolean - The corresponding  boolean  value.
### listIndent() {#listIndent--}
```
public void listIndent()
```


Increases the list level of the current paragraph by one level.

This method changes the list level and applies formatting properties of the new level.

In Word documents, lists may consist of up to nine levels. List formatting for each level specifies what bullet or number is used, left indent, space between the bullet and text etc.

### listOutdent() {#listOutdent--}
```
public void listOutdent()
```


Decreases the list level of the current paragraph by one level.

This method changes the list level and applies formatting properties of the new level.

In Word documents, lists may consist of up to nine levels. List formatting for each level specifies what bullet or number is used, left indent, space between the bullet and text etc.

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### removeNumbers() {#removeNumbers--}
```
public void removeNumbers()
```


Removes numbers or bullets from the current paragraph and sets list level to zero.

Calling this method is equivalent to setting the [getList()](../../com.aspose.words/listformat\#getList--) / [setList(com.aspose.words.List)](../../com.aspose.words/listformat\#setList-com.aspose.words.List-) property to null.

### setList(List value) {#setList-com.aspose.words.List-}
```
public void setList(List value)
```


Sets the list this paragraph is a member of.

The list that is being assigned to this property must belong to the current document.

The list that is being assigned to this property must not be a list style definition.

Setting this property to null removes bullets and numbering from the paragraph and sets the list level number to zero. Setting this property to null is equivalent to calling [removeNumbers()](../../com.aspose.words/listformat\#removeNumbers--).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [List](../../com.aspose.words/list) | The list this paragraph is a member of. |

### setListLevelNumber(int value) {#setListLevelNumber-int-}
```
public void setListLevelNumber(int value)
```


Sets the list level number (0 to 8) for the paragraph.

In Word documents, lists may consist of 1 or 9 levels, numbered 0 to 8.

Has effect only when the [getList()](../../com.aspose.words/listformat\#getList--) / [setList(com.aspose.words.List)](../../com.aspose.words/listformat\#setList-com.aspose.words.List-) property is set to reference a valid list.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The list level number (0 to 8) for the paragraph. |

### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

