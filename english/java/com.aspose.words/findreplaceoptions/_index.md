---
title: FindReplaceOptions
second_title: Aspose.Words for Java API Reference
description: Specifies options for find/replace operations.
type: docs
weight: 270
url: /java/com.aspose.words/findreplaceoptions/
---

**Inheritance:**
java.lang.Object
```
public class FindReplaceOptions
```

Specifies options for find/replace operations.

To learn more, visit the **Find and Replace** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [FindReplaceOptions()](#FindReplaceOptions--) | Initializes a new instance of this class. |
| [FindReplaceOptions(int direction)](#FindReplaceOptions-int-) | Initializes a new instance of this class. |
| [FindReplaceOptions(IReplacingCallback replacingCallback)](#FindReplaceOptions-com.aspose.words.IReplacingCallback-) | Initializes a new instance of this class. |
| [FindReplaceOptions(int direction, IReplacingCallback replacingCallback)](#FindReplaceOptions-int-com.aspose.words.IReplacingCallback-) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getApplyFont()](#getApplyFont--) | Text formatting applied to new content. |
| [getApplyParagraphFormat()](#getApplyParagraphFormat--) | Paragraph formatting applied to new content. |
| [getClass()](#getClass--) |  |
| [getDirection()](#getDirection--) | Selects direction for replace. |
| [getFindWholeWordsOnly()](#getFindWholeWordsOnly--) | True indicates the oldValue must be a standalone word. |
| [getIgnoreDeleted()](#getIgnoreDeleted--) | Gets a boolean value indicating either to ignore text inside delete revisions. |
| [getIgnoreFieldCodes()](#getIgnoreFieldCodes--) | Gets a boolean value indicating either to ignore text inside field codes. |
| [getIgnoreFields()](#getIgnoreFields--) | Gets a boolean value indicating either to ignore text inside fields. |
| [getIgnoreFootnotes()](#getIgnoreFootnotes--) | Gets a boolean value indicating either to ignore footnotes. |
| [getIgnoreInserted()](#getIgnoreInserted--) | Gets a boolean value indicating either to ignore text inside insert revisions. |
| [getIgnoreStructuredDocumentTags()](#getIgnoreStructuredDocumentTags--) | Gets a boolean value indicating either to ignore content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag). |
| [getLegacyMode()](#getLegacyMode--) | Gets a boolean value indicating that old find/replace algorithm is used. |
| [getMatchCase()](#getMatchCase--) | True indicates case-sensitive comparison, false indicates case-insensitive comparison. |
| [getReplacingCallback()](#getReplacingCallback--) | The user-defined method which is called before every replace occurrence. |
| [getSmartParagraphBreakReplacement()](#getSmartParagraphBreakReplacement--) | Gets or sets a boolean value indicating either it is allowed to replace paragraph break when there is no next sibling paragraph. |
| [getUseLegacyOrder()](#getUseLegacyOrder--) | True indicates that a text search is performed sequentially from top to bottom considering the text boxes. |
| [getUseSubstitutions()](#getUseSubstitutions--) | Gets a boolean value indicating whether to recognize and use substitutions within replacement patterns. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setDirection(int value)](#setDirection-int-) | Selects direction for replace. |
| [setFindWholeWordsOnly(boolean value)](#setFindWholeWordsOnly-boolean-) | True indicates the oldValue must be a standalone word. |
| [setIgnoreDeleted(boolean value)](#setIgnoreDeleted-boolean-) | Sets a boolean value indicating either to ignore text inside delete revisions. |
| [setIgnoreFieldCodes(boolean value)](#setIgnoreFieldCodes-boolean-) | Sets a boolean value indicating either to ignore text inside field codes. |
| [setIgnoreFields(boolean value)](#setIgnoreFields-boolean-) | Sets a boolean value indicating either to ignore text inside fields. |
| [setIgnoreFootnotes(boolean value)](#setIgnoreFootnotes-boolean-) | Sets a boolean value indicating either to ignore footnotes. |
| [setIgnoreInserted(boolean value)](#setIgnoreInserted-boolean-) | Sets a boolean value indicating either to ignore text inside insert revisions. |
| [setIgnoreStructuredDocumentTags(boolean value)](#setIgnoreStructuredDocumentTags-boolean-) | Sets a boolean value indicating either to ignore content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag). |
| [setLegacyMode(boolean value)](#setLegacyMode-boolean-) | Sets a boolean value indicating that old find/replace algorithm is used. |
| [setMatchCase(boolean value)](#setMatchCase-boolean-) | True indicates case-sensitive comparison, false indicates case-insensitive comparison. |
| [setReplacingCallback(IReplacingCallback value)](#setReplacingCallback-com.aspose.words.IReplacingCallback-) | The user-defined method which is called before every replace occurrence. |
| [setSmartParagraphBreakReplacement(boolean value)](#setSmartParagraphBreakReplacement-boolean-) | Gets or sets a boolean value indicating either it is allowed to replace paragraph break when there is no next sibling paragraph. |
| [setUseLegacyOrder(boolean value)](#setUseLegacyOrder-boolean-) | True indicates that a text search is performed sequentially from top to bottom considering the text boxes. |
| [setUseSubstitutions(boolean value)](#setUseSubstitutions-boolean-) | Sets a boolean value indicating whether to recognize and use substitutions within replacement patterns. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### FindReplaceOptions() {#FindReplaceOptions--}
```
public FindReplaceOptions()
```


Initializes a new instance of this class.

### FindReplaceOptions(int direction) {#FindReplaceOptions-int-}
```
public FindReplaceOptions(int direction)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| direction | int |  |

### FindReplaceOptions(IReplacingCallback replacingCallback) {#FindReplaceOptions-com.aspose.words.IReplacingCallback-}
```
public FindReplaceOptions(IReplacingCallback replacingCallback)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| replacingCallback | [IReplacingCallback](../../com.aspose.words/ireplacingcallback) |  |

### FindReplaceOptions(int direction, IReplacingCallback replacingCallback) {#FindReplaceOptions-int-com.aspose.words.IReplacingCallback-}
```
public FindReplaceOptions(int direction, IReplacingCallback replacingCallback)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| direction | int |  |
| replacingCallback | [IReplacingCallback](../../com.aspose.words/ireplacingcallback) |  |

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
### getApplyFont() {#getApplyFont--}
```
public Font getApplyFont()
```


Text formatting applied to new content.

**Returns:**
[Font](../../com.aspose.words/font) - The corresponding [Font](../../com.aspose.words/font) value.
### getApplyParagraphFormat() {#getApplyParagraphFormat--}
```
public ParagraphFormat getApplyParagraphFormat()
```


Paragraph formatting applied to new content.

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - The corresponding [ParagraphFormat](../../com.aspose.words/paragraphformat) value.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getDirection() {#getDirection--}
```
public int getDirection()
```


Selects direction for replace. Default value is [FindReplaceDirection.FORWARD](../../com.aspose.words/findreplacedirection\#FORWARD).

**Returns:**
int - The corresponding  int  value. The returned value is one of [FindReplaceDirection](../../com.aspose.words/findreplacedirection) constants.
### getFindWholeWordsOnly() {#getFindWholeWordsOnly--}
```
public boolean getFindWholeWordsOnly()
```


True indicates the oldValue must be a standalone word.

**Returns:**
boolean - The corresponding  boolean  value.
### getIgnoreDeleted() {#getIgnoreDeleted--}
```
public boolean getIgnoreDeleted()
```


Gets a boolean value indicating either to ignore text inside delete revisions. The default value is  false .

**Returns:**
boolean - A boolean value indicating either to ignore text inside delete revisions.
### getIgnoreFieldCodes() {#getIgnoreFieldCodes--}
```
public boolean getIgnoreFieldCodes()
```


Gets a boolean value indicating either to ignore text inside field codes. The default value is  false .

This option affects only field codes (it does not ignore nodes between [NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype\#FIELD-SEPARATOR) and [NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END)).

To ignore whole field, please use corresponding option [getIgnoreFields()](../../com.aspose.words/findreplaceoptions\#getIgnoreFields--) / [setIgnoreFields(boolean)](../../com.aspose.words/findreplaceoptions\#setIgnoreFields-boolean-).

**Returns:**
boolean - A boolean value indicating either to ignore text inside field codes.
### getIgnoreFields() {#getIgnoreFields--}
```
public boolean getIgnoreFields()
```


Gets a boolean value indicating either to ignore text inside fields. The default value is  false .

This option affects whole field (all nodes between [NodeType.FIELD\_START](../../com.aspose.words/nodetype\#FIELD-START) and [NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END)).

To ignore only field codes, please use corresponding option [getIgnoreFieldCodes()](../../com.aspose.words/findreplaceoptions\#getIgnoreFieldCodes--) / [setIgnoreFieldCodes(boolean)](../../com.aspose.words/findreplaceoptions\#setIgnoreFieldCodes-boolean-).

**Returns:**
boolean - A boolean value indicating either to ignore text inside fields.
### getIgnoreFootnotes() {#getIgnoreFootnotes--}
```
public boolean getIgnoreFootnotes()
```


Gets a boolean value indicating either to ignore footnotes. The default value is  false .

**Returns:**
boolean - A boolean value indicating either to ignore footnotes.
### getIgnoreInserted() {#getIgnoreInserted--}
```
public boolean getIgnoreInserted()
```


Gets a boolean value indicating either to ignore text inside insert revisions. The default value is  false .

**Returns:**
boolean - A boolean value indicating either to ignore text inside insert revisions.
### getIgnoreStructuredDocumentTags() {#getIgnoreStructuredDocumentTags--}
```
public boolean getIgnoreStructuredDocumentTags()
```


Gets a boolean value indicating either to ignore content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag). The default value is  false .

When this option is set to  true , the content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) will be treated as a simple text.

Otherwise, [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) will be processed as standalone Story and replacing pattern will be searched separately for each [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag), so that if pattern crosses a [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag), then replacement will not be performed for such pattern.

**Returns:**
boolean - A boolean value indicating either to ignore content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag).
### getLegacyMode() {#getLegacyMode--}
```
public boolean getLegacyMode()
```


Gets a boolean value indicating that old find/replace algorithm is used. Use this flag if you need exactly the same behavior as before advanced find/replace feature was introduced. Note that old algorithm does not support advanced features such as replace with breaks, apply formatting and so on.

**Returns:**
boolean - A boolean value indicating that old find/replace algorithm is used.
### getMatchCase() {#getMatchCase--}
```
public boolean getMatchCase()
```


True indicates case-sensitive comparison, false indicates case-insensitive comparison.

**Returns:**
boolean - The corresponding  boolean  value.
### getReplacingCallback() {#getReplacingCallback--}
```
public IReplacingCallback getReplacingCallback()
```


The user-defined method which is called before every replace occurrence.

**Returns:**
[IReplacingCallback](../../com.aspose.words/ireplacingcallback) - The corresponding [IReplacingCallback](../../com.aspose.words/ireplacingcallback) value.
### getSmartParagraphBreakReplacement() {#getSmartParagraphBreakReplacement--}
```
public boolean getSmartParagraphBreakReplacement()
```


Gets or sets a boolean value indicating either it is allowed to replace paragraph break when there is no next sibling paragraph.

The default value is  false .

This option allows to replace paragraph break when there is no next sibling paragraph to which all child nodes can be moved, by finding any (not necessarily sibling) next paragraph after the paragraph being replaced.

**Returns:**
boolean - The corresponding  boolean  value.
### getUseLegacyOrder() {#getUseLegacyOrder--}
```
public boolean getUseLegacyOrder()
```


True indicates that a text search is performed sequentially from top to bottom considering the text boxes. Default value is false.

**Returns:**
boolean - The corresponding  boolean  value.
### getUseSubstitutions() {#getUseSubstitutions--}
```
public boolean getUseSubstitutions()
```


Gets a boolean value indicating whether to recognize and use substitutions within replacement patterns. The default value is  false . For the details on substitution elements please refer to: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

**Returns:**
boolean - A boolean value indicating whether to recognize and use substitutions within replacement patterns.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setDirection(int value) {#setDirection-int-}
```
public void setDirection(int value)
```


Selects direction for replace. Default value is [FindReplaceDirection.FORWARD](../../com.aspose.words/findreplacedirection\#FORWARD).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [FindReplaceDirection](../../com.aspose.words/findreplacedirection) constants. |

### setFindWholeWordsOnly(boolean value) {#setFindWholeWordsOnly-boolean-}
```
public void setFindWholeWordsOnly(boolean value)
```


True indicates the oldValue must be a standalone word.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setIgnoreDeleted(boolean value) {#setIgnoreDeleted-boolean-}
```
public void setIgnoreDeleted(boolean value)
```


Sets a boolean value indicating either to ignore text inside delete revisions. The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating either to ignore text inside delete revisions. |

### setIgnoreFieldCodes(boolean value) {#setIgnoreFieldCodes-boolean-}
```
public void setIgnoreFieldCodes(boolean value)
```


Sets a boolean value indicating either to ignore text inside field codes. The default value is  false .

This option affects only field codes (it does not ignore nodes between [NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype\#FIELD-SEPARATOR) and [NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END)).

To ignore whole field, please use corresponding option [getIgnoreFields()](../../com.aspose.words/findreplaceoptions\#getIgnoreFields--) / [setIgnoreFields(boolean)](../../com.aspose.words/findreplaceoptions\#setIgnoreFields-boolean-).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating either to ignore text inside field codes. |

### setIgnoreFields(boolean value) {#setIgnoreFields-boolean-}
```
public void setIgnoreFields(boolean value)
```


Sets a boolean value indicating either to ignore text inside fields. The default value is  false .

This option affects whole field (all nodes between [NodeType.FIELD\_START](../../com.aspose.words/nodetype\#FIELD-START) and [NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END)).

To ignore only field codes, please use corresponding option [getIgnoreFieldCodes()](../../com.aspose.words/findreplaceoptions\#getIgnoreFieldCodes--) / [setIgnoreFieldCodes(boolean)](../../com.aspose.words/findreplaceoptions\#setIgnoreFieldCodes-boolean-).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating either to ignore text inside fields. |

### setIgnoreFootnotes(boolean value) {#setIgnoreFootnotes-boolean-}
```
public void setIgnoreFootnotes(boolean value)
```


Sets a boolean value indicating either to ignore footnotes. The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating either to ignore footnotes. |

### setIgnoreInserted(boolean value) {#setIgnoreInserted-boolean-}
```
public void setIgnoreInserted(boolean value)
```


Sets a boolean value indicating either to ignore text inside insert revisions. The default value is  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating either to ignore text inside insert revisions. |

### setIgnoreStructuredDocumentTags(boolean value) {#setIgnoreStructuredDocumentTags-boolean-}
```
public void setIgnoreStructuredDocumentTags(boolean value)
```


Sets a boolean value indicating either to ignore content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag). The default value is  false .

When this option is set to  true , the content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) will be treated as a simple text.

Otherwise, [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) will be processed as standalone Story and replacing pattern will be searched separately for each [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag), so that if pattern crosses a [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag), then replacement will not be performed for such pattern.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating either to ignore content of [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag). |

### setLegacyMode(boolean value) {#setLegacyMode-boolean-}
```
public void setLegacyMode(boolean value)
```


Sets a boolean value indicating that old find/replace algorithm is used. Use this flag if you need exactly the same behavior as before advanced find/replace feature was introduced. Note that old algorithm does not support advanced features such as replace with breaks, apply formatting and so on.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating that old find/replace algorithm is used. |

### setMatchCase(boolean value) {#setMatchCase-boolean-}
```
public void setMatchCase(boolean value)
```


True indicates case-sensitive comparison, false indicates case-insensitive comparison.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setReplacingCallback(IReplacingCallback value) {#setReplacingCallback-com.aspose.words.IReplacingCallback-}
```
public void setReplacingCallback(IReplacingCallback value)
```


The user-defined method which is called before every replace occurrence.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IReplacingCallback](../../com.aspose.words/ireplacingcallback) | The corresponding [IReplacingCallback](../../com.aspose.words/ireplacingcallback) value. |

### setSmartParagraphBreakReplacement(boolean value) {#setSmartParagraphBreakReplacement-boolean-}
```
public void setSmartParagraphBreakReplacement(boolean value)
```


Gets or sets a boolean value indicating either it is allowed to replace paragraph break when there is no next sibling paragraph.

The default value is  false .

This option allows to replace paragraph break when there is no next sibling paragraph to which all child nodes can be moved, by finding any (not necessarily sibling) next paragraph after the paragraph being replaced.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setUseLegacyOrder(boolean value) {#setUseLegacyOrder-boolean-}
```
public void setUseLegacyOrder(boolean value)
```


True indicates that a text search is performed sequentially from top to bottom considering the text boxes. Default value is false.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setUseSubstitutions(boolean value) {#setUseSubstitutions-boolean-}
```
public void setUseSubstitutions(boolean value)
```


Sets a boolean value indicating whether to recognize and use substitutions within replacement patterns. The default value is  false . For the details on substitution elements please refer to: https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating whether to recognize and use substitutions within replacement patterns. |

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

