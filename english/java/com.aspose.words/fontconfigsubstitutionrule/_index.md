---
title: FontConfigSubstitutionRule
linktitle: FontConfigSubstitutionRule
second_title: Aspose.Words for Java API Reference
description: Font config substitution rule in Java.
type: docs
weight: 278
url: /java/com.aspose.words/fontconfigsubstitutionrule/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSubstitutionRule](../../com.aspose.words/fontsubstitutionrule/)
```
public class FontConfigSubstitutionRule extends FontSubstitutionRule
```

Font config substitution rule.

To learn more, visit the [ Working with Fonts ][Working with Fonts] documentation article.

This rule uses fontconfig utility on Linux (and other Unix-like) platforms to get the substitution if the original font is not available.

If fontconfig utility is not available then this rule will be ignored.


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getEnabled()](#getEnabled) | Specifies whether the rule is enabled or not. |
| [hashCode()](#hashCode) |  |
| [isFontConfigAvailable()](#isFontConfigAvailable) | Check if fontconfig utility is available or not. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [resetCache()](#resetCache) | Resets the cache of fontconfig calling results. |
| [setEnabled(boolean value)](#setEnabled-boolean) | Specifies whether the rule is enabled or not. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getEnabled() {#getEnabled}
```
public boolean getEnabled()
```


Specifies whether the rule is enabled or not.

**Returns:**
boolean - The corresponding  boolean  value.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isFontConfigAvailable() {#isFontConfigAvailable}
```
public boolean isFontConfigAvailable()
```


Check if fontconfig utility is available or not.

**Returns:**
boolean
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### resetCache() {#resetCache}
```
public void resetCache()
```


Resets the cache of fontconfig calling results.

### setEnabled(boolean value) {#setEnabled-boolean}
```
public void setEnabled(boolean value)
```


Specifies whether the rule is enabled or not.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

