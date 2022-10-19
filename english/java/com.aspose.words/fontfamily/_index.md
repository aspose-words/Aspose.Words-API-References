---
title: FontFamily
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 278
url: /java/com.aspose.words/fontfamily/
---

**Inheritance:**
java.lang.Object
```
public class FontFamily
```

A utility class providing constants. Represents the font family.

A font family is a set of fonts having common stroke width and serif characteristics.
## Fields

| Field | Description |
| --- | --- |
| [AUTO](#AUTO) | Specifies a generic family name. |
| [ROMAN](#ROMAN) | Specifies a proportional font with serifs. |
| [SWISS](#SWISS) | Specifies a proportional font without serifs. |
| [MODERN](#MODERN) | Specifies a monospace font with or without serifs. |
| [SCRIPT](#SCRIPT) | Specifies a font that is designed to look like handwriting; examples include Script and Cursive. |
| [DECORATIVE](#DECORATIVE) | Specifies a novelty font. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int fontFamily)](#getName-int-) |  |
| [toString(int fontFamily)](#toString-int-) |  |
| [fromName(String fontFamilyName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Specifies a generic family name. This name is used when information about a font does not exist or does not matter. The default font is used.

### ROMAN {#ROMAN}
```
public static int ROMAN
```


Specifies a proportional font with serifs. An example is Times New Roman.

### SWISS {#SWISS}
```
public static int SWISS
```


Specifies a proportional font without serifs. An example is Arial.

### MODERN {#MODERN}
```
public static int MODERN
```


Specifies a monospace font with or without serifs. Monospace fonts are usually modern; examples include Pica, Elite, and Courier New.

### SCRIPT {#SCRIPT}
```
public static int SCRIPT
```


Specifies a font that is designed to look like handwriting; examples include Script and Cursive.

### DECORATIVE {#DECORATIVE}
```
public static int DECORATIVE
```


Specifies a novelty font. An example is Old English.

### length {#length}
```
public static int length
```


### getName(int fontFamily) {#getName-int-}
```
public static String getName(int fontFamily)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontFamily | int |  |

**Returns:**
java.lang.String
### toString(int fontFamily) {#toString-int-}
```
public static String toString(int fontFamily)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontFamily | int |  |

**Returns:**
java.lang.String
### fromName(String fontFamilyName) {#fromName-java.lang.String-}
```
public static int fromName(String fontFamilyName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontFamilyName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
