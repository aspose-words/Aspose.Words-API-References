---
title: SvgTextOutputMode
second_title: Aspose.Words for Java API Reference
description: 
type: docs
weight: 542
url: /java/com.aspose.words/svgtextoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class SvgTextOutputMode
```
## Fields

| Field | Description |
| --- | --- |
| [USE_SVG_FONTS](#USE-SVG-FONTS) | SVG fonts are used to render text. |
| [USE_TARGET_MACHINE_FONTS](#USE-TARGET-MACHINE-FONTS) | Fonts installed on the target machine are used to render text. |
| [USE_PLACED_GLYPHS](#USE-PLACED-GLYPHS) | Text is rendered using curves. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int svgTextOutputMode)](#getName-int-) |  |
| [toString(int svgTextOutputMode)](#toString-int-) |  |
| [fromName(String svgTextOutputModeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### USE_SVG_FONTS {#USE-SVG-FONTS}
```
public static int USE_SVG_FONTS
```


SVG fonts are used to render text. Note, not all browsers support SVG fonts.

### USE_TARGET_MACHINE_FONTS {#USE-TARGET-MACHINE-FONTS}
```
public static int USE_TARGET_MACHINE_FONTS
```


Fonts installed on the target machine are used to render text. Note, if some of fonts used in the document are not available on the target machine, document can look differently.

### USE_PLACED_GLYPHS {#USE-PLACED-GLYPHS}
```
public static int USE_PLACED_GLYPHS
```


Text is rendered using curves. Note, text selection will not work if you use this option.

### length {#length}
```
public static int length
```


### getName(int svgTextOutputMode) {#getName-int-}
```
public static String getName(int svgTextOutputMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| svgTextOutputMode | int |  |

**Returns:**
java.lang.String
### toString(int svgTextOutputMode) {#toString-int-}
```
public static String toString(int svgTextOutputMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| svgTextOutputMode | int |  |

**Returns:**
java.lang.String
### fromName(String svgTextOutputModeName) {#fromName-java.lang.String-}
```
public static int fromName(String svgTextOutputModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| svgTextOutputModeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
