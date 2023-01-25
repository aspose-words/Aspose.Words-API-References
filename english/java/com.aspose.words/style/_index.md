---
title: Style
second_title: Aspose.Words for Java API Reference
description: Represents a single built-in or user-defined style.
type: docs
weight: 540
url: /java/com.aspose.words/style/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Style implements Cloneable
```

Represents a single built-in or user-defined style.

To learn more, visit the [ Working with Styles and Themes ][Working with Styles and Themes] documentation article.


[Working with Styles and Themes]: https://docs.aspose.com/words/java/working-with-styles-and-themes/
## Methods

| Method | Description |
| --- | --- |
| [clearParaAttrs()](#clearParaAttrs) |  |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [equals(Style style)](#equals-com.aspose.words.Style) | Compares with the specified style. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int) |  |
| [getAliases()](#getAliases) | Gets all aliases of this style. |
| [getBaseStyleName()](#getBaseStyleName) | Gets/sets the name of the style this style is based on. |
| [getBuiltIn()](#getBuiltIn) | True if this style is one of the built-in styles in MS Word. |
| [getClass()](#getClass) |  |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Gets the owner document. |
| [getFont()](#getFont) | Gets the character formatting of the style. |
| [getLinkedStyleName()](#getLinkedStyleName) | Gets the name of the [Style](../../com.aspose.words/style) linked to this one. |
| [getList()](#getList) | Gets the list that defines formatting of this list style. |
| [getListFormat()](#getListFormat) | Provides access to the list formatting properties of a paragraph style. |
| [getName()](#getName) | Gets the name of the style. |
| [getNextParagraphStyleName()](#getNextParagraphStyleName) | Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style. |
| [getParagraphFormat()](#getParagraphFormat) | Gets the paragraph formatting of the style. |
| [getStyleIdentifier()](#getStyleIdentifier) | Gets the locale independent style identifier for a built-in style. |
| [getStyles()](#getStyles) | Gets the collection of styles this style belongs to. |
| [getType()](#getType) | Gets the style type (paragraph or character). |
| [hashCode()](#hashCode) |  |
| [isHeading()](#isHeading) | True when the style is one of the built-in Heading styles. |
| [isQuickStyle()](#isQuickStyle) | Specifies whether this style is shown in the Quick Style gallery inside MS Word UI. |
| [isQuickStyle(boolean value)](#isQuickStyle-boolean) | Specifies whether this style is shown in the Quick Style gallery inside MS Word UI. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove()](#remove) | Removes the specified style from the document. |
| [removeParaAttr(int key)](#removeParaAttr-int) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [setBaseStyleName(String value)](#setBaseStyleName-java.lang.String) | Gets/sets the name of the style this style is based on. |
| [setName(String value)](#setName-java.lang.String) | Sets the name of the style. |
| [setNextParagraphStyleName(String value)](#setNextParagraphStyleName-java.lang.String) | Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object) |  |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### clearParaAttrs() {#clearParaAttrs}
```
public void clearParaAttrs()
```




### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### equals(Style style) {#equals-com.aspose.words.Style}
```
public boolean equals(Style style)
```


Compares with the specified style. Styles Istds are compared for built-in styles only. Styles defaults are not included in comparison. Base style, linked style and next paragraph style are recursively compared.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style) |  |

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
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int}
```
public Object fetchInheritedParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
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
### fetchParaAttr(int key) {#fetchParaAttr-int}
```
public Object fetchParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAliases() {#getAliases}
```
public String[] getAliases()
```


Gets all aliases of this style. If style has no aliases then empty array of string is returned.

**Returns:**
java.lang.String[] - All aliases of this style.
### getBaseStyleName() {#getBaseStyleName}
```
public String getBaseStyleName()
```


Gets/sets the name of the style this style is based on. This will be an empty string if the style is not based on any other style and it can be set to an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getBuiltIn() {#getBuiltIn}
```
public boolean getBuiltIn()
```


True if this style is one of the built-in styles in MS Word.

**Returns:**
boolean - The corresponding  boolean  value.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getDirectParaAttr(int key) {#getDirectParaAttr-int}
```
public Object getDirectParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
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
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Gets the owner document.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase) - The owner document.
### getFont() {#getFont}
```
public Font getFont()
```


Gets the character formatting of the style.

For list styles this property returns  null .

**Returns:**
[Font](../../com.aspose.words/font) - The character formatting of the style.
### getLinkedStyleName() {#getLinkedStyleName}
```
public String getLinkedStyleName()
```


Gets the name of the [Style](../../com.aspose.words/style) linked to this one. Returns empty string if no styles are linked.

**Returns:**
java.lang.String - The name of the [Style](../../com.aspose.words/style) linked to this one.
### getList() {#getList}
```
public List getList()
```


Gets the list that defines formatting of this list style.

This property is only valid for list styles. For other style types this property returns  null .

**Returns:**
[List](../../com.aspose.words/list) - The list that defines formatting of this list style.
### getListFormat() {#getListFormat}
```
public ListFormat getListFormat()
```


Provides access to the list formatting properties of a paragraph style.

This property is only valid for paragraph styles. For other style types this property returns  null .

**Returns:**
[ListFormat](../../com.aspose.words/listformat) - The corresponding [ListFormat](../../com.aspose.words/listformat) value.
### getName() {#getName}
```
public String getName()
```


Gets the name of the style.

Can not be empty string.

If there already is a style with such name in the collection, then this style will override it. All affected nodes will reference new style.

**Returns:**
java.lang.String - The name of the style.
### getNextParagraphStyleName() {#getNextParagraphStyleName}
```
public String getNextParagraphStyleName()
```


Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style. This property is not used by Aspose.Words. The next paragraph style will only be applied automatically when you edit the document in MS Word.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getParagraphFormat() {#getParagraphFormat}
```
public ParagraphFormat getParagraphFormat()
```


Gets the paragraph formatting of the style.

For character and list styles this property returns  null .

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - The paragraph formatting of the style.
### getStyleIdentifier() {#getStyleIdentifier}
```
public int getStyleIdentifier()
```


Gets the locale independent style identifier for a built-in style.

For user defined (custom) styles, this property returns [StyleIdentifier.USER](../../com.aspose.words/styleidentifier\#USER).

**Returns:**
int - The locale independent style identifier for a built-in style. The returned value is one of [StyleIdentifier](../../com.aspose.words/styleidentifier) constants.
### getStyles() {#getStyles}
```
public StyleCollection getStyles()
```


Gets the collection of styles this style belongs to.

**Returns:**
[StyleCollection](../../com.aspose.words/stylecollection) - The collection of styles this style belongs to.
### getType() {#getType}
```
public int getType()
```


Gets the style type (paragraph or character).

**Returns:**
int - The style type (paragraph or character). The returned value is one of [StyleType](../../com.aspose.words/styletype) constants.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isHeading() {#isHeading}
```
public boolean isHeading()
```


True when the style is one of the built-in Heading styles.

**Returns:**
boolean - The corresponding  boolean  value.
### isQuickStyle() {#isQuickStyle}
```
public boolean isQuickStyle()
```


Specifies whether this style is shown in the Quick Style gallery inside MS Word UI.

**Returns:**
boolean - The corresponding  boolean  value.
### isQuickStyle(boolean value) {#isQuickStyle-boolean}
```
public void isQuickStyle(boolean value)
```


Specifies whether this style is shown in the Quick Style gallery inside MS Word UI.

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




### remove() {#remove}
```
public void remove()
```


Removes the specified style from the document. Style removal has following effects on the document model:

 *  All references to the style are removed from corresponding paragraphs, runs and tables.
 *  If base style is removed its formatting is moved to child styles.
 *  If style to be deleted has a linked style, then both of these are deleted.

### removeParaAttr(int key) {#removeParaAttr-int}
```
public void removeParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### setBaseStyleName(String value) {#setBaseStyleName-java.lang.String}
```
public void setBaseStyleName(String value)
```


Gets/sets the name of the style this style is based on. This will be an empty string if the style is not based on any other style and it can be set to an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Sets the name of the style.

Can not be empty string.

If there already is a style with such name in the collection, then this style will override it. All affected nodes will reference new style.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the style. |

### setNextParagraphStyleName(String value) {#setNextParagraphStyleName-java.lang.String}
```
public void setNextParagraphStyleName(String value)
```


Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style. This property is not used by Aspose.Words. The next paragraph style will only be applied automatically when you edit the document in MS Word.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object}
```
public void setParaAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

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

