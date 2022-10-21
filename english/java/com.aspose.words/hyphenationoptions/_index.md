---
title: HyphenationOptions
second_title: Aspose.Words for Java API Reference
description: Allows to configure document hyphenation options.
type: docs
weight: 334
url: /java/com.aspose.words/hyphenationoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class HyphenationOptions implements Cloneable
```

Allows to configure document hyphenation options.

To learn more, visit the **Working with Hyphenation** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getAutoHyphenation()](#getAutoHyphenation--) | Gets value determining whether automatic hyphenation is turned on for the document. |
| [setAutoHyphenation(boolean value)](#setAutoHyphenation-boolean-) | Sets value determining whether automatic hyphenation is turned on for the document. |
| [getConsecutiveHyphenLimit()](#getConsecutiveHyphenLimit--) | Gets the maximum number of consecutive lines that can end with hyphens. |
| [setConsecutiveHyphenLimit(int value)](#setConsecutiveHyphenLimit-int-) | Sets the maximum number of consecutive lines that can end with hyphens. |
| [getHyphenationZone()](#getHyphenationZone--) | Gets the distance in 1/20 of a point from the right margin within which you do not want to hyphenate words. |
| [setHyphenationZone(int value)](#setHyphenationZone-int-) | Sets the distance in 1/20 of a point from the right margin within which you do not want to hyphenate words. |
| [getHyphenateCaps()](#getHyphenateCaps--) | Gets value determining whether words written in all capital letters are hyphenated. |
| [setHyphenateCaps(boolean value)](#setHyphenateCaps-boolean-) | Sets value determining whether words written in all capital letters are hyphenated. |
### getAutoHyphenation() {#getAutoHyphenation--}
```
public boolean getAutoHyphenation()
```


Gets value determining whether automatic hyphenation is turned on for the document. Default value for this property is **false**.

**Returns:**
boolean - Value determining whether automatic hyphenation is turned on for the document.
### setAutoHyphenation(boolean value) {#setAutoHyphenation-boolean-}
```
public void setAutoHyphenation(boolean value)
```


Sets value determining whether automatic hyphenation is turned on for the document. Default value for this property is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Value determining whether automatic hyphenation is turned on for the document. |

### getConsecutiveHyphenLimit() {#getConsecutiveHyphenLimit--}
```
public int getConsecutiveHyphenLimit()
```


Gets the maximum number of consecutive lines that can end with hyphens. Default value for this property is 0.

If value of this property is set to 0, any number of consecutive lines can end with hyphens.

The property does not have effect when saving to fixed page formats e.g. PDF.

**Returns:**
int - The maximum number of consecutive lines that can end with hyphens.
### setConsecutiveHyphenLimit(int value) {#setConsecutiveHyphenLimit-int-}
```
public void setConsecutiveHyphenLimit(int value)
```


Sets the maximum number of consecutive lines that can end with hyphens. Default value for this property is 0.

If value of this property is set to 0, any number of consecutive lines can end with hyphens.

The property does not have effect when saving to fixed page formats e.g. PDF.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The maximum number of consecutive lines that can end with hyphens. |

### getHyphenationZone() {#getHyphenationZone--}
```
public int getHyphenationZone()
```


Gets the distance in 1/20 of a point from the right margin within which you do not want to hyphenate words. Default value for this property is 360 (0.25 inch).

**Returns:**
int - The distance in 1/20 of a point from the right margin within which you do not want to hyphenate words.
### setHyphenationZone(int value) {#setHyphenationZone-int-}
```
public void setHyphenationZone(int value)
```


Sets the distance in 1/20 of a point from the right margin within which you do not want to hyphenate words. Default value for this property is 360 (0.25 inch).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The distance in 1/20 of a point from the right margin within which you do not want to hyphenate words. |

### getHyphenateCaps() {#getHyphenateCaps--}
```
public boolean getHyphenateCaps()
```


Gets value determining whether words written in all capital letters are hyphenated. Default value for this property is **true**.

**Returns:**
boolean - Value determining whether words written in all capital letters are hyphenated.
### setHyphenateCaps(boolean value) {#setHyphenateCaps-boolean-}
```
public void setHyphenateCaps(boolean value)
```


Sets value determining whether words written in all capital letters are hyphenated. Default value for this property is **true**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | Value determining whether words written in all capital letters are hyphenated. |

