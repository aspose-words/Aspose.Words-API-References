---
title: Style
second_title: Aspose.Words for Java API Reference
description: Represents a single built-in or user-defined style.
type: docs
weight: 536
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

To learn more, visit the **Working with Styles and Themes** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getName()](#getName--) | Gets the name of the style. |
| [setName(String value)](#setName-java.lang.String-) | Sets the name of the style. |
| [getStyleIdentifier()](#getStyleIdentifier--) | Gets the locale independent style identifier for a built-in style. |
| [getAliases()](#getAliases--) | Gets all aliases of this style. |
| [isHeading()](#isHeading--) | True when the style is one of the built-in Heading styles. |
| [getType()](#getType--) | Gets the style type (paragraph or character). |
| [getDocument()](#getDocument--) | Gets the owner document. |
| [getLinkedStyleName()](#getLinkedStyleName--) | Gets the name of the Style linked to this one. |
| [getBaseStyleName()](#getBaseStyleName--) | Gets/sets the name of the style this style is based on. |
| [setBaseStyleName(String value)](#setBaseStyleName-java.lang.String-) | Gets/sets the name of the style this style is based on. |
| [getNextParagraphStyleName()](#getNextParagraphStyleName--) | Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style. |
| [setNextParagraphStyleName(String value)](#setNextParagraphStyleName-java.lang.String-) | Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style. |
| [getBuiltIn()](#getBuiltIn--) | True if this style is one of the built-in styles in MS Word. |
| [getFont()](#getFont--) | Gets the character formatting of the style. |
| [getParagraphFormat()](#getParagraphFormat--) | Gets the paragraph formatting of the style. |
| [getList()](#getList--) | Gets the list that defines formatting of this list style. |
| [getListFormat()](#getListFormat--) | Provides access to the list formatting properties of a paragraph style. |
| [isQuickStyle()](#isQuickStyle--) | Specifies whether this style is shown in the Quick Style gallery inside MS Word UI. |
| [isQuickStyle(boolean value)](#isQuickStyle-boolean-) | Specifies whether this style is shown in the Quick Style gallery inside MS Word UI. |
| [getStyles()](#getStyles--) | Gets the collection of styles this style belongs to. |
| [remove()](#remove--) | Removes the specified style from the document. |
| [equals(Style style)](#equals-com.aspose.words.Style-) | Compares with the specified style. |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int-) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int-) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int-) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int-) |  |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object-) |  |
| [removeParaAttr(int key)](#removeParaAttr-int-) |  |
| [clearParaAttrs()](#clearParaAttrs--) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
### getName() {#getName--}
```
public String getName()
```


Gets the name of the style.

Can not be empty string.

If there already is a style with such name in the collection, then this style will override it. All affected nodes will reference new style.

**Returns:**
java.lang.String - The name of the style.
### setName(String value) {#setName-java.lang.String-}
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

### getStyleIdentifier() {#getStyleIdentifier--}
```
public int getStyleIdentifier()
```


Gets the locale independent style identifier for a built-in style.

For user defined (custom) styles, this property returns [StyleIdentifier.USER](../../com.aspose.words/styleidentifier\#USER).

**Returns:**
int - The locale independent style identifier for a built-in style. The returned value is one of [StyleIdentifier](../../com.aspose.words/styleidentifier) constants.
### getAliases() {#getAliases--}
```
public String[] getAliases()
```


Gets all aliases of this style. If style has no aliases then empty array of string is returned.

**Returns:**
java.lang.String[] - All aliases of this style.
### isHeading() {#isHeading--}
```
public boolean isHeading()
```


True when the style is one of the built-in Heading styles.

**Returns:**
boolean - The corresponding  boolean  value.
### getType() {#getType--}
```
public int getType()
```


Gets the style type (paragraph or character).

**Returns:**
int - The style type (paragraph or character). The returned value is one of [StyleType](../../com.aspose.words/styletype) constants.
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Gets the owner document.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase) - The owner document.
### getLinkedStyleName() {#getLinkedStyleName--}
```
public String getLinkedStyleName()
```


Gets the name of the Style linked to this one. Returns Empty string if no styles are linked.

**Returns:**
java.lang.String - The name of the Style linked to this one.
### getBaseStyleName() {#getBaseStyleName--}
```
public String getBaseStyleName()
```


Gets/sets the name of the style this style is based on. This will be an empty string if the style is not based on any other style and it can be set to an empty string.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setBaseStyleName(String value) {#setBaseStyleName-java.lang.String-}
```
public void setBaseStyleName(String value)
```


Gets/sets the name of the style this style is based on. This will be an empty string if the style is not based on any other style and it can be set to an empty string.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getNextParagraphStyleName() {#getNextParagraphStyleName--}
```
public String getNextParagraphStyleName()
```


Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style. This property is not used by Aspose.Words. The next paragraph style will only be applied automatically when you edit the document in MS Word.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setNextParagraphStyleName(String value) {#setNextParagraphStyleName-java.lang.String-}
```
public void setNextParagraphStyleName(String value)
```


Gets/sets the name of the style to be applied automatically to a new paragraph inserted after a paragraph formatted with the specified style. This property is not used by Aspose.Words. The next paragraph style will only be applied automatically when you edit the document in MS Word.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

### getBuiltIn() {#getBuiltIn--}
```
public boolean getBuiltIn()
```


True if this style is one of the built-in styles in MS Word.

**Returns:**
boolean - The corresponding  boolean  value.
### getFont() {#getFont--}
```
public Font getFont()
```


Gets the character formatting of the style.

For list styles this property returns null.

**Returns:**
[Font](../../com.aspose.words/font) - The character formatting of the style.
### getParagraphFormat() {#getParagraphFormat--}
```
public ParagraphFormat getParagraphFormat()
```


Gets the paragraph formatting of the style.

For character and list styles this property returns null.

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - The paragraph formatting of the style.
### getList() {#getList--}
```
public List getList()
```


Gets the list that defines formatting of this list style.

This property is only valid for list styles. For other style types this property returns null.

**Returns:**
[List](../../com.aspose.words/list) - The list that defines formatting of this list style.
### getListFormat() {#getListFormat--}
```
public ListFormat getListFormat()
```


Provides access to the list formatting properties of a paragraph style.

This property is only valid for paragraph styles. For other style types this property returns null.

**Returns:**
[ListFormat](../../com.aspose.words/listformat) - The corresponding [ListFormat](../../com.aspose.words/listformat) value.
### isQuickStyle() {#isQuickStyle--}
```
public boolean isQuickStyle()
```


Specifies whether this style is shown in the Quick Style gallery inside MS Word UI.

**Returns:**
boolean - The corresponding  boolean  value.
### isQuickStyle(boolean value) {#isQuickStyle-boolean-}
```
public void isQuickStyle(boolean value)
```


Specifies whether this style is shown in the Quick Style gallery inside MS Word UI.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getStyles() {#getStyles--}
```
public StyleCollection getStyles()
```


Gets the collection of styles this style belongs to.

**Returns:**
[StyleCollection](../../com.aspose.words/stylecollection) - The collection of styles this style belongs to.
### remove() {#remove--}
```
public void remove()
```


Removes the specified style from the document. Style removal has following effects on the document model:

 *  All references to the style are removed from corresponding paragraphs, runs and tables.
 *  If base style is removed its formatting is moved to child styles.
 *  If style to be deleted has a linked style, then both of these are deleted.

### equals(Style style) {#equals-com.aspose.words.Style-}
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
### getDirectParaAttr(int key) {#getDirectParaAttr-int-}
```
public Object getDirectParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int-}
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
### fetchParaAttr(int key) {#fetchParaAttr-int-}
```
public Object fetchParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int-}
```
public Object fetchInheritedParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object-}
```
public void setParaAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### removeParaAttr(int key) {#removeParaAttr-int-}
```
public void removeParaAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

### clearParaAttrs() {#clearParaAttrs--}
```
public void clearParaAttrs()
```




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




