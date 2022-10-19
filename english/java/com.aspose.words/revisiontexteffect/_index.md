---
title: RevisionTextEffect
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 489
url: /java/com.aspose.words/revisiontexteffect/
---

**Inheritance:**
java.lang.Object
```
public class RevisionTextEffect
```

A utility class providing constants. Allows to specify decoration effect for revisions of document text.
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | Revised content has no special effects applied. |
| [COLOR](#COLOR) | Revised content is highlighted with color only. |
| [BOLD](#BOLD) | Revised content is made bold and colored. |
| [ITALIC](#ITALIC) | Revised content is made italic and colored. |
| [UNDERLINE](#UNDERLINE) | Revised content is underlined and colored. |
| [DOUBLE_UNDERLINE](#DOUBLE-UNDERLINE) | Revised content is double underlined and colored. |
| [STRIKE_THROUGH](#STRIKE-THROUGH) | Revised content is stroked through and colored. |
| [DOUBLE_STRIKE_THROUGH](#DOUBLE-STRIKE-THROUGH) | Revised content is double stroked through and colored. |
| [HIDDEN](#HIDDEN) | Revised content is hidden. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int revisionTextEffect)](#getName-int-) |  |
| [toString(int revisionTextEffect)](#toString-int-) |  |
| [fromName(String revisionTextEffectName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### NONE {#NONE}
```
public static int NONE
```


Revised content has no special effects applied. This corresponds to [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT).

### COLOR {#COLOR}
```
public static int COLOR
```


Revised content is highlighted with color only.

### BOLD {#BOLD}
```
public static int BOLD
```


Revised content is made bold and colored.

### ITALIC {#ITALIC}
```
public static int ITALIC
```


Revised content is made italic and colored.

### UNDERLINE {#UNDERLINE}
```
public static int UNDERLINE
```


Revised content is underlined and colored.

### DOUBLE_UNDERLINE {#DOUBLE-UNDERLINE}
```
public static int DOUBLE_UNDERLINE
```


Revised content is double underlined and colored.

### STRIKE_THROUGH {#STRIKE-THROUGH}
```
public static int STRIKE_THROUGH
```


Revised content is stroked through and colored.

### DOUBLE_STRIKE_THROUGH {#DOUBLE-STRIKE-THROUGH}
```
public static int DOUBLE_STRIKE_THROUGH
```


Revised content is double stroked through and colored. Only works for [RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION), [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) and [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING) ('move from' type).

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


Revised content is hidden. Only works for [RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION) and [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING) ('move from' type).

### length {#length}
```
public static int length
```


### getName(int revisionTextEffect) {#getName-int-}
```
public static String getName(int revisionTextEffect)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionTextEffect | int |  |

**Returns:**
java.lang.String
### toString(int revisionTextEffect) {#toString-int-}
```
public static String toString(int revisionTextEffect)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionTextEffect | int |  |

**Returns:**
java.lang.String
### fromName(String revisionTextEffectName) {#fromName-java.lang.String-}
```
public static int fromName(String revisionTextEffectName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionTextEffectName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
