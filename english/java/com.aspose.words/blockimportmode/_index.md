---
title: BlockImportMode
linktitle: BlockImportMode
second_title: Aspose.Words for Java
description: Specifies how properties of block-level elements are imported from HTML-based documents in Java.
type: docs
weight: 29
url: /java/com.aspose.words/blockimportmode/
---

**Inheritance:**
java.lang.Object
```
public class BlockImportMode
```

Specifies how properties of block-level elements are imported from HTML-based documents.

 **Examples:** 

Shows how properties of block-level elements are imported from HTML-based documents.

```

 final String html = "\n\n \n \n paragraph 1\n paragraph 2\n\n\n";

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();
 // Set the new mode of import HTML block-level elements.
 loadOptions.setBlockImportMode(blockImportMode);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), loadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BlockImport.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [MERGE](#MERGE) | Properties of parent blocks are merged and stored on child elements (i.e. |
| [PRESERVE](#PRESERVE) | Properties of parent blocks are imported to a special logical structure and are stored separately from document nodes. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String blockImportModeName)](#fromName-java.lang.String) |  |
| [getName(int blockImportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int blockImportMode)](#toString-int) |  |
### MERGE {#MERGE}
```
public static int MERGE
```


Properties of parent blocks are merged and stored on child elements (i.e. paragraphs or tables).

 **Remarks:** 

Properties of parent blocks are merged as follows: margins are added together; borders of higher-level blocks are discarded and only the most inner-level borders are preserved. As a result, when this mode is specified, some formatting of blocks from the original document will be lost.

On the other hand, since all merged block-level properties are stored on document nodes, all formating in the resulting document will be available for modification.

### PRESERVE {#PRESERVE}
```
public static int PRESERVE
```


Properties of parent blocks are imported to a special logical structure and are stored separately from document nodes.

 **Remarks:** 

Only margins and borders of 'body', 'div', and 'blockquote' HTML elements are imported. Properties of each HTML element are stored individually.

This mode allows to better preserve borders and margins seen in the HTML document and get better conversion results. The downside is that the resulting document gets harder to modify, since borders and margins stored in the logical structure are not available for editing.

This mode mimics MS Word's behavior regarding import of block properties.

### length {#length}
```
public static int length
```


### fromName(String blockImportModeName) {#fromName-java.lang.String}
```
public static int fromName(String blockImportModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| blockImportModeName | java.lang.String |  |

**Returns:**
int
### getName(int blockImportMode) {#getName-int}
```
public static String getName(int blockImportMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| blockImportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int blockImportMode) {#toString-int}
```
public static String toString(int blockImportMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| blockImportMode | int |  |

**Returns:**
java.lang.String
