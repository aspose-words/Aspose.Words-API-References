---
title: FontInfoCollection
second_title: Aspose.Words for Java API Reference
description: Represents a collection of fonts used in a document.
type: docs
weight: 281
url: /java/com.aspose.words/fontinfocollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class FontInfoCollection implements Iterable
```

Represents a collection of fonts used in a document.

To learn more, visit the **Working with Fonts** documentation article.

Items are [FontInfo](../../com.aspose.words/fontinfo) objects.

You do not create instances of this class directly. Use the [DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--) property to access the collection of fonts defined in the document.
## Methods

| Method | Description |
| --- | --- |
| [contains(String name)](#contains-java.lang.String-) | Determines whether the collection contains a font with the given name. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | Gets a font at the specified index. |
| [get(String name)](#get-java.lang.String-) | Provides access to the collection items. |
| [getClass()](#getClass--) |  |
| [getCount()](#getCount--) | Gets the number of elements contained in the collection. |
| [getEmbedSystemFonts()](#getEmbedSystemFonts--) | Specifies whether or not to embed System fonts into the document. |
| [getEmbedTrueTypeFonts()](#getEmbedTrueTypeFonts--) | Specifies whether or not to embed TrueType fonts in a document when it is saved. |
| [getSaveSubsetFonts()](#getSaveSubsetFonts--) | Specifies whether or not to save a subset of the embedded TrueType fonts with the document. |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | Returns an iterator object that can be used to iterate over all items in the collection. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setEmbedSystemFonts(boolean value)](#setEmbedSystemFonts-boolean-) | Specifies whether or not to embed System fonts into the document. |
| [setEmbedTrueTypeFonts(boolean value)](#setEmbedTrueTypeFonts-boolean-) | Specifies whether or not to embed TrueType fonts in a document when it is saved. |
| [setSaveSubsetFonts(boolean value)](#setSaveSubsetFonts-boolean-) | Specifies whether or not to save a subset of the embedded TrueType fonts with the document. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


Determines whether the collection contains a font with the given name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | Case-insensitive name of the font to locate. |

**Returns:**
boolean - True if the item is found in the collection; otherwise, false.
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
### get(int index) {#get-int-}
```
public FontInfo get(int index)
```


Gets a font at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | Zero-based index of the font. |

**Returns:**
[FontInfo](../../com.aspose.words/fontinfo) - A font at the specified index.
### get(String name) {#get-java.lang.String-}
```
public FontInfo get(String name)
```


Provides access to the collection items.  Gets a font with the specified name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | Case-insensitive name of the font to locate. |

**Returns:**
[FontInfo](../../com.aspose.words/fontinfo) - The corresponding [FontInfo](../../com.aspose.words/fontinfo) value.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCount() {#getCount--}
```
public int getCount()
```


Gets the number of elements contained in the collection.

**Returns:**
int - The number of elements contained in the collection.
### getEmbedSystemFonts() {#getEmbedSystemFonts--}
```
public boolean getEmbedSystemFonts()
```


Specifies whether or not to embed System fonts into the document. Default value for this property is **false**.

This option works only when [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-) option is set to **true**.

Setting this property to  True  is useful if the user is on an East Asian system and wants to create a document that is readable by others who do not have fonts for that language on their system. For example, a user on a Japanese system could choose to embed the fonts in a document so that the Japanese document would be readable on all systems.

This option works for DOC, DOCX and RTF formats only.

**Returns:**
boolean - The corresponding  boolean  value.
### getEmbedTrueTypeFonts() {#getEmbedTrueTypeFonts--}
```
public boolean getEmbedTrueTypeFonts()
```


Specifies whether or not to embed TrueType fonts in a document when it is saved. Default value for this property is **false**.

Embedding TrueType fonts allows others to view the document with the same fonts that were used to create it, but may substantially increase the document size.

This option works for DOC, DOCX and RTF formats only.

**Returns:**
boolean - The corresponding  boolean  value.
### getSaveSubsetFonts() {#getSaveSubsetFonts--}
```
public boolean getSaveSubsetFonts()
```


Specifies whether or not to save a subset of the embedded TrueType fonts with the document. Default value for this property is **false**.

This option works only when [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-) property is set to **true**.

This option works for DOC, DOCX and RTF formats only.

**Returns:**
boolean - The corresponding  boolean  value.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an iterator object that can be used to iterate over all items in the collection.

**Returns:**
java.util.Iterator
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setEmbedSystemFonts(boolean value) {#setEmbedSystemFonts-boolean-}
```
public void setEmbedSystemFonts(boolean value)
```


Specifies whether or not to embed System fonts into the document. Default value for this property is **false**.

This option works only when [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-) option is set to **true**.

Setting this property to  True  is useful if the user is on an East Asian system and wants to create a document that is readable by others who do not have fonts for that language on their system. For example, a user on a Japanese system could choose to embed the fonts in a document so that the Japanese document would be readable on all systems.

This option works for DOC, DOCX and RTF formats only.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setEmbedTrueTypeFonts(boolean value) {#setEmbedTrueTypeFonts-boolean-}
```
public void setEmbedTrueTypeFonts(boolean value)
```


Specifies whether or not to embed TrueType fonts in a document when it is saved. Default value for this property is **false**.

Embedding TrueType fonts allows others to view the document with the same fonts that were used to create it, but may substantially increase the document size.

This option works for DOC, DOCX and RTF formats only.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setSaveSubsetFonts(boolean value) {#setSaveSubsetFonts-boolean-}
```
public void setSaveSubsetFonts(boolean value)
```


Specifies whether or not to save a subset of the embedded TrueType fonts with the document. Default value for this property is **false**.

This option works only when [getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-) property is set to **true**.

This option works for DOC, DOCX and RTF formats only.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

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

