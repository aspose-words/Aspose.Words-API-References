---
title: HtmlInsertOptions
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 327
url: /java/com.aspose.words/htmlinsertoptions/
---

**Inheritance:**
java.lang.Object
```
public class HtmlInsertOptions
```

A utility class providing constants. Specifies options for the **M:Aspose.Words.DocumentBuilder.InsertHtml(System.String,Aspose.Words.HtmlInsertOptions)** method.
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | Use the default options when inserting HTML. |
| [USE_BUILDER_FORMATTING](#USE-BUILDER-FORMATTING) | Use font and paragraph formatting specified in [DocumentBuilder](../../com.aspose.words/documentbuilder) as base formatting for text inserted from HTML. |
| [REMOVE_LAST_EMPTY_PARAGRAPH](#REMOVE-LAST-EMPTY-PARAGRAPH) | Remove the empty paragraph that is normally inserted after HTML that ends with a block-level element. |
| [PRESERVE_BLOCKS](#PRESERVE-BLOCKS) | Preserve properties of block-level elements. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int htmlInsertOptions)](#getName-int-) |  |
| [getNames(int htmlInsertOptions)](#getNames-int-) |  |
| [toString(int htmlInsertOptions)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [fromName(String htmlInsertOptionsName)](#fromName-java.lang.String-) |  |
| [fromNames(Set htmlInsertOptionsNames)](#fromNames-java.util.Set-) |  |
| [getValues()](#getValues--) |  |
### NONE {#NONE}
```
public static int NONE
```


Use the default options when inserting HTML.

### USE_BUILDER_FORMATTING {#USE-BUILDER-FORMATTING}
```
public static int USE_BUILDER_FORMATTING
```


Use font and paragraph formatting specified in [DocumentBuilder](../../com.aspose.words/documentbuilder) as base formatting for text inserted from HTML.

If this option is not specified, formatting of [DocumentBuilder](../../com.aspose.words/documentbuilder) is ignored and text is inserted with default HTML formatting. As a result, the text looks as it is rendered in browsers.

If this option is specified, formatting of inserted text is based on formatting specified in [DocumentBuilder](../../com.aspose.words/documentbuilder), and the text looks as if it were inserted using [DocumentBuilder.write(java.lang.String)](../../com.aspose.words/documentbuilder\#write-java.lang.String-).

### REMOVE_LAST_EMPTY_PARAGRAPH {#REMOVE-LAST-EMPTY-PARAGRAPH}
```
public static int REMOVE_LAST_EMPTY_PARAGRAPH
```


Remove the empty paragraph that is normally inserted after HTML that ends with a block-level element. By default, [DocumentBuilder](../../com.aspose.words/documentbuilder) makes sure that the last block-level element imported from HTML is closed after import and inserts a paragraph break after the element. This paragraph break separates content imported from HTML from content of the template document. However, if a HTML fragment is inserted into an empty paragraph, that paragraph break will create an extra empty paragraph. If this behavior is undesired, specify this option.

### PRESERVE_BLOCKS {#PRESERVE-BLOCKS}
```
public static int PRESERVE_BLOCKS
```


Preserve properties of block-level elements.

By default, properties of parent blocks are merged and stored on their child elements (i.e. paragraphs or tables). If this option is specified, properties of each block are stored separately in a special logical structure. As a result, this option allows to better preserve individual borders and margins seen in the HTML document and get better conversion results. The downside is that the resulting document gets harder to modify, since borders and margins stored in the logical structure are not available for editing.

Only margins and borders of 'body', 'div', and 'blockquote' HTML elements are preserved. Properties of each HTML element are stored separately.

If this option is specified, Aspose.Words mimics MS Word's behavior regarding import of block properties.

### length {#length}
```
public static int length
```


### getName(int htmlInsertOptions) {#getName-int-}
```
public static String getName(int htmlInsertOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.lang.String
### getNames(int htmlInsertOptions) {#getNames-int-}
```
public static Set getNames(int htmlInsertOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.util.Set
### toString(int htmlInsertOptions) {#toString-int-}
```
public static String toString(int htmlInsertOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int-}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
### fromName(String htmlInsertOptionsName) {#fromName-java.lang.String-}
```
public static int fromName(String htmlInsertOptionsName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlInsertOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set htmlInsertOptionsNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set htmlInsertOptionsNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlInsertOptionsNames | java.util.Set |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
