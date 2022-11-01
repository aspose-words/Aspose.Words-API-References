---
title: List
second_title: Aspose.Words for Java API Reference
description: Represents formatting of a list.
type: docs
weight: 368
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

To learn more, visit the **Working with Lists** documentation article.

A list in a Microsoft Word document is a set of list formatting properties. Each list can have up to 9 levels and formatting properties, such as number style, start value, indent, tab position etc are defined separately for each level.

A [List](../../com.aspose.words/list) object always belongs to the [ListCollection](../../com.aspose.words/listcollection) collection.

To create a new list, use the Add methods of the [ListCollection](../../com.aspose.words/listcollection) collection.

To modify formatting of a list, use [ListLevel](../../com.aspose.words/listlevel) objects found in the [getListLevels()](../../com.aspose.words/list\#getListLevels--) collection.

To apply or remove list formatting from a paragraph, use [ListFormat](../../com.aspose.words/listformat).
## Methods

| Method | Description |
| --- | --- |
| [compareTo(List other)](#compareTo-com.aspose.words.List-) | Compares the specified list to the current list. |
| [equals(List list)](#equals-com.aspose.words.List-) | Compares with the specified list. |
| [equals(Object obj)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDocument()](#getDocument--) | Gets the owner document. |
| [getListId()](#getListId--) | Gets the unique identifier of the list. |
| [getListLevels()](#getListLevels--) | Gets the collection of list levels for this list. |
| [getStyle()](#getStyle--) | Gets the list style that this list references or defines. |
| [hasSameTemplate(List other)](#hasSameTemplate-com.aspose.words.List-) | Returns true if the current list and the given list are created from the same template. |
| [hashCode()](#hashCode--) |  |
| [isListStyleDefinition()](#isListStyleDefinition--) | Returns true if this list is a definition of a list style. |
| [isListStyleReference()](#isListStyleReference--) | Returns true if this list is a reference to a list style. |
| [isMultiLevel()](#isMultiLevel--) | Returns true when the list contains 9 levels; false when 1 level. |
| [isRestartAtEachSection()](#isRestartAtEachSection--) | Specifies whether list should be restarted at each section. |
| [isRestartAtEachSection(boolean value)](#isRestartAtEachSection-boolean-) | Specifies whether list should be restarted at each section. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### compareTo(List other) {#compareTo-com.aspose.words.List-}
```
public int compareTo(List other)
```


Compares the specified list to the current list.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| other | [List](../../com.aspose.words/list) |  |

**Returns:**
int
### equals(List list) {#equals-com.aspose.words.List-}
```
public boolean equals(List list)
```


Compares with the specified list.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| list | [List](../../com.aspose.words/list) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Gets the owner document.

A list always has a parent document and is valid only in the context of that document.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase) - The owner document.
### getListId() {#getListId--}
```
public int getListId()
```


Gets the unique identifier of the list.

You do not normally need to use this property. But if you use it, you normally do so in conjunction with the [ListCollection.getListByListId(int)](../../com.aspose.words/listcollection\#getListByListId-int-) method to find a list by its identifier.

**Returns:**
int - The unique identifier of the list.
### getListLevels() {#getListLevels--}
```
public ListLevelCollection getListLevels()
```


Gets the collection of list levels for this list.

Use this property to access and modify formatting individual to each level of the list.

**Returns:**
[ListLevelCollection](../../com.aspose.words/listlevelcollection) - The collection of list levels for this list.
### getStyle() {#getStyle--}
```
public Style getStyle()
```


Gets the list style that this list references or defines.

If this list is not associated with a list style, the property will return null.

A list could be a reference to a list style, in this case [isListStyleReference()](../../com.aspose.words/list\#isListStyleReference--) will be true.

A list could be a definition of a list style, in this case [isListStyleDefinition()](../../com.aspose.words/list\#isListStyleDefinition--) will be true. Such a list cannot be applied to paragraphs in the document directly.

**Returns:**
[Style](../../com.aspose.words/style) - The list style that this list references or defines.
### hasSameTemplate(List other) {#hasSameTemplate-com.aspose.words.List-}
```
public boolean hasSameTemplate(List other)
```


Returns true if the current list and the given list are created from the same template.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| other | [List](../../com.aspose.words/list) |  |

**Returns:**
boolean
### hashCode() {#hashCode--}
```
public int hashCode()
```




**Returns:**
int
### isListStyleDefinition() {#isListStyleDefinition--}
```
public boolean isListStyleDefinition()
```


Returns true if this list is a definition of a list style.

When this property is true, the [getStyle()](../../com.aspose.words/list\#getStyle--) property returns the list style that this list defines.

By modifying properties of a list that defines a list style, you modify the properties of the list style.

A list that is a definition of a list style cannot be applied directly to paragraphs to make them numbered.

**Returns:**
boolean - True if this list is a definition of a list style.
### isListStyleReference() {#isListStyleReference--}
```
public boolean isListStyleReference()
```


Returns true if this list is a reference to a list style.

Note, modifying properties of a list that is a reference to list style has no effect. The list formatting specified in the list style itself always takes precedence.

**Returns:**
boolean - True if this list is a reference to a list style.
### isMultiLevel() {#isMultiLevel--}
```
public boolean isMultiLevel()
```


Returns true when the list contains 9 levels; false when 1 level.

The lists that you create with Aspose.Words are always multi-level lists and contain 9 levels.

Microsoft Word 2003 and later always create multi-level lists with 9 levels. But in some documents, created with earlier versions of Microsoft Word you might encounter lists that have 1 level only.

**Returns:**
boolean - True when the list contains 9 levels; false when 1 level.
### isRestartAtEachSection() {#isRestartAtEachSection--}
```
public boolean isRestartAtEachSection()
```


Specifies whether list should be restarted at each section. Default value is **false**.

This option is supported only in RTF, DOC and DOCX document formats.

This option will be written to DOCX only if [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance) is higher then [OoxmlCompliance.ECMA\_376\_2006](../../com.aspose.words/ooxmlcompliance\#ECMA-376-2006).

**Returns:**
boolean - The corresponding  boolean  value.
### isRestartAtEachSection(boolean value) {#isRestartAtEachSection-boolean-}
```
public void isRestartAtEachSection(boolean value)
```


Specifies whether list should be restarted at each section. Default value is **false**.

This option is supported only in RTF, DOC and DOCX document formats.

This option will be written to DOCX only if [OoxmlCompliance](../../com.aspose.words/ooxmlcompliance) is higher then [OoxmlCompliance.ECMA\_376\_2006](../../com.aspose.words/ooxmlcompliance\#ECMA-376-2006).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




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

