---
title: ExportListLabels
second_title: Aspose.Words for Java API Reference
description: Specifies how list labels are exported to HTML MHTML and EPUB.
type: docs
weight: 150
url: /java/com.aspose.words/exportlistlabels/
---

**Inheritance:**
java.lang.Object
```
public class ExportListLabels
```

Specifies how list labels are exported to HTML, MHTML and EPUB.
## Fields

| Field | Description |
| --- | --- |
| [AUTO](#AUTO) | Outputs list labels in auto mode. |
| [AS_INLINE_TEXT](#AS-INLINE-TEXT) | Outputs all list labels as inline text. |
| [BY_HTML_TAGS](#BY-HTML-TAGS) | Outputs all list labels as HTML native elements. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int exportListLabels)](#getName-int-) |  |
| [toString(int exportListLabels)](#toString-int-) |  |
| [fromName(String exportListLabelsName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Outputs list labels in auto mode. Uses HTML native elements when possible. HTML

 *  tags are used for list label representation if it doesn't cause formatting loss, otherwise the HTML
    
    tag is used.

### AS_INLINE_TEXT {#AS-INLINE-TEXT}
```
public static int AS_INLINE_TEXT
```


Outputs all list labels as inline text. HTML

tag is used for any list label representation.

### BY_HTML_TAGS {#BY-HTML-TAGS}
```
public static int BY_HTML_TAGS
```


Outputs all list labels as HTML native elements. HTML

 *  tags are used for list label representation. Some formatting loss is possible.

### length {#length}
```
public static int length
```


### getName(int exportListLabels) {#getName-int-}
```
public static String getName(int exportListLabels)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| exportListLabels | int |  |

**Returns:**
java.lang.String
### toString(int exportListLabels) {#toString-int-}
```
public static String toString(int exportListLabels)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| exportListLabels | int |  |

**Returns:**
java.lang.String
### fromName(String exportListLabelsName) {#fromName-java.lang.String-}
```
public static int fromName(String exportListLabelsName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| exportListLabelsName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
