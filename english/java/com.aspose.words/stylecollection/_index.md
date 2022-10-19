---
title: StyleCollection
second_title: Aspose.Words for Java API Reference
description: A collection of Style objects that represent both the built-in and user-defined styles in a document.
type: docs
weight: 537
url: /java/com.aspose.words/stylecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable, java.lang.Iterable
```
public class StyleCollection implements Cloneable, Iterable
```

A collection of Style objects that represent both the built-in and user-defined styles in a document.

To learn more, visit the **Working with Styles and Themes** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [clearQuickStyleGallery()](#clearQuickStyleGallery--) | Removes all styles from the Quick Style Gallery panel. |
| [getDocument()](#getDocument--) | Gets the owner document. |
| [getDefaultFont()](#getDefaultFont--) | Gets document default text formatting. |
| [getDefaultParagraphFormat()](#getDefaultParagraphFormat--) | Gets document default paragraph formatting. |
| [getCount()](#getCount--) | Gets the number of styles in the collection. |
| [get(String name)](#get-java.lang.String-) | Retrieves a style from the collection. |
| [getByStyleIdentifier(int sti)](#getByStyleIdentifier-int-) |  |
| [get(int index)](#get-int-) | Gets a style by index. |
| [iterator()](#iterator--) | Gets an enumerator object that will enumerate styles in the alphabetical order of their names. |
| [add(int type, String name)](#add-int-java.lang.String-) |  |
| [addCopy(Style style)](#addCopy-com.aspose.words.Style-) | Copies a style into this collection. |
### clearQuickStyleGallery() {#clearQuickStyleGallery--}
```
public void clearQuickStyleGallery()
```


Removes all styles from the Quick Style Gallery panel.

### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Gets the owner document.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase) - The owner document.
### getDefaultFont() {#getDefaultFont--}
```
public Font getDefaultFont()
```


Gets document default text formatting.

Note that document-wide defaults were introduced in Microsoft Word 2007 and are fully supported in OOXML formats ( [LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX)) only. Earlier document formats have limited support for this feature and only font names can be stored.

**Returns:**
[Font](../../com.aspose.words/font) - Document default text formatting.
### getDefaultParagraphFormat() {#getDefaultParagraphFormat--}
```
public ParagraphFormat getDefaultParagraphFormat()
```


Gets document default paragraph formatting.

Note that document-wide defaults were introduced in Microsoft Word 2007 and are fully supported in OOXML formats ( [LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX)) only. Earlier document formats have no support for document default paragraph formatting.

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - Document default paragraph formatting.
### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of styles in the collection.

**Returns:**
int - The number of styles in the collection.
### get(String name) {#get-java.lang.String-}
```
public Style get(String name)
```


Retrieves a style from the collection.  Gets a style by name or alias.

Case sensitive, returns null if the style with the given name is not found.

If this is an English name of a built in style that does not yet exist, automatically creates it.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
[Style](../../com.aspose.words/style) - The corresponding [Style](../../com.aspose.words/style) value.
### getByStyleIdentifier(int sti) {#getByStyleIdentifier-int-}
```
public Style getByStyleIdentifier(int sti)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sti | int |  |

**Returns:**
[Style](../../com.aspose.words/style)
### get(int index) {#get-int-}
```
public Style get(int index)
```


Gets a style by index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[Style](../../com.aspose.words/style) - A style by index.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Gets an enumerator object that will enumerate styles in the alphabetical order of their names.

**Returns:**
java.util.Iterator
### add(int type, String name) {#add-int-java.lang.String-}
```
public Style add(int type, String name)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| type | int |  |
| name | java.lang.String |  |

**Returns:**
[Style](../../com.aspose.words/style)
### addCopy(Style style) {#addCopy-com.aspose.words.Style-}
```
public Style addCopy(Style style)
```


Copies a style into this collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style) | Style to be copied. |

**Returns:**
[Style](../../com.aspose.words/style) - Copied style ready for usage.

Style to be copied can belong to the same document as well as to different document.

Linked style is copied.

This method does doesn't copy base styles.

If collection already contains a style with the same name, then new name is automatically generated by adding "\_number" suffix starting from 0 e.g. "Normal\_0", "Heading 1\_1" etc. Use [Style.getName()](../../com.aspose.words/style\#getName--) / [Style.setName(java.lang.String)](../../com.aspose.words/style\#setName-java.lang.String-) setter for changing the name of the imported style.