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
| [USE_PLACED_GLYPHS](#USE-PLACED-GLYPHS) | Text is rendered using curves. |
| [USE_SVG_FONTS](#USE-SVG-FONTS) | SVG fonts are used to render text. |
| [USE_TARGET_MACHINE_FONTS](#USE-TARGET-MACHINE-FONTS) | Fonts installed on the target machine are used to render text. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String svgTextOutputModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int svgTextOutputMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int svgTextOutputMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### USE_PLACED_GLYPHS {#USE-PLACED-GLYPHS}
```
public static int USE_PLACED_GLYPHS
```


Text is rendered using curves. Note, text selection will not work if you use this option.

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

### length {#length}
```
public static int length
```


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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
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
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
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




### toString() {#toString--}
```
public String toString()
```




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

