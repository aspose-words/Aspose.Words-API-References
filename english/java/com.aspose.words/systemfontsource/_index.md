---
title: SystemFontSource
second_title: Aspose.Words for Java API Reference
description: Represents all TrueType fonts installed to the system.
type: docs
weight: 546
url: /java/com.aspose.words/systemfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase)
```
public class SystemFontSource extends FontSourceBase
```

Represents all TrueType fonts installed to the system.

To learn more, visit the [ Working with Fonts ][Working with Fonts] documentation article.


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Constructors

| Constructor | Description |
| --- | --- |
| [SystemFontSource()](#SystemFontSource) | Ctor. |
| [SystemFontSource(int priority)](#SystemFontSource-int) | Ctor. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getAvailableFonts()](#getAvailableFonts) | Returns list of fonts available via this source. |
| [getClass()](#getClass) |  |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | Returns the font source priority. |
| [getPriorityInternal()](#getPriorityInternal) |  |
| [getSystemFontFolders()](#getSystemFontFolders) | Returns system font folders or empty array if folders are not accessible. |
| [getType()](#getType) | Returns the type of the font source. |
| [getWarningCallback()](#getWarningCallback) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### SystemFontSource() {#SystemFontSource}
```
public SystemFontSource()
```


Ctor.

### SystemFontSource(int priority) {#SystemFontSource-int}
```
public SystemFontSource(int priority)
```


Ctor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| priority | int | Font source priority. See the [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase\#getPriority) property description for more information. |

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
### getAvailableFonts() {#getAvailableFonts}
```
public ArrayList getAvailableFonts()
```


Returns list of fonts available via this source.

**Returns:**
java.util.ArrayList
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getFontDataInternal() {#getFontDataInternal}
```
public Iterable getFontDataInternal()
```




**Returns:**
java.lang.Iterable
### getPriority() {#getPriority}
```
public int getPriority()
```


Returns the font source priority.

This value is used when there are fonts with the same family name and style in different font sources. In this case Aspose.Words selects the font from the source with the higher priority value.

The default value is 0.

**Returns:**
int - The font source priority.
### getPriorityInternal() {#getPriorityInternal}
```
public int getPriorityInternal()
```




**Returns:**
int
### getSystemFontFolders() {#getSystemFontFolders}
```
public static String[] getSystemFontFolders()
```


Returns system font folders or empty array if folders are not accessible. On some platforms Aspose.Words could search system fonts not only through folders but in other sources too. For example, on Windows platform Aspose.Words search fonts also in the registry.

**Returns:**
java.lang.String[]
### getType() {#getType}
```
public int getType()
```


Returns the type of the font source.

**Returns:**
int - The type of the font source. The returned value is one of [FontSourceType](../../com.aspose.words/fontsourcetype) constants.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Called during processing of font source when an issue is detected that might result in formatting fidelity loss.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback) value.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback}
```
public void setWarningCallback(IWarningCallback value)
```


Called during processing of font source when an issue is detected that might result in formatting fidelity loss.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback) | The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback) value. |

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

