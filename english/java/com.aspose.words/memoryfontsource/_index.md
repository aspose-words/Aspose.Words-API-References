---
title: MemoryFontSource
linktitle: MemoryFontSource
second_title: Aspose.Words for Java API Reference
description: Represents the single TrueType font file stored in memory in Java.
type: docs
weight: 399
url: /java/com.aspose.words/memoryfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase/)
```
public class MemoryFontSource extends FontSourceBase
```

Represents the single TrueType font file stored in memory.

To learn more, visit the [ Working with Fonts ][Working with Fonts] documentation article.


[Working with Fonts]: https://docs.aspose.com/words/java/working-with-fonts/
## Constructors

| Constructor | Description |
| --- | --- |
| [MemoryFontSource(byte[] fontData)](#MemoryFontSource-byte) | Ctor. |
| [MemoryFontSource(byte[] fontData, int priority)](#MemoryFontSource-byte---int) | Ctor. |
| [MemoryFontSource(byte[] fontData, int priority, String cacheKey)](#MemoryFontSource-byte---int-java.lang.String) | Ctor. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getAvailableFonts()](#getAvailableFonts) | Returns list of fonts available via this source. |
| [getCacheKey()](#getCacheKey) | The key of this source in the cache. |
| [getClass()](#getClass) |  |
| [getFontData()](#getFontData) | Binary font data. |
| [getFontDataInternal()](#getFontDataInternal) |  |
| [getPriority()](#getPriority) | Returns the font source priority. |
| [getPriorityInternal()](#getPriorityInternal) |  |
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
### MemoryFontSource(byte[] fontData) {#MemoryFontSource-byte}
```
public MemoryFontSource(byte[] fontData)
```


Ctor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontData | byte[] | Binary font data. |

### MemoryFontSource(byte[] fontData, int priority) {#MemoryFontSource-byte---int}
```
public MemoryFontSource(byte[] fontData, int priority)
```


Ctor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontData | byte[] | Binary font data. |
| priority | int | Font source priority. See the [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) property description for more information. |

### MemoryFontSource(byte[] fontData, int priority, String cacheKey) {#MemoryFontSource-byte---int-java.lang.String}
```
public MemoryFontSource(byte[] fontData, int priority, String cacheKey)
```


Ctor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontData | byte[] | Binary font data. |
| priority | int | Font source priority. See the [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase/\#getPriority) property description for more information. |
| cacheKey | java.lang.String | The key of this source in the cache. See [getCacheKey()](../../com.aspose.words/memoryfontsource/\#getCacheKey) property description for more information. |

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
### getCacheKey() {#getCacheKey}
```
public String getCacheKey()
```


The key of this source in the cache. This key is used to identify cache item when saving/loading font search cache with  and  methods.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getFontData() {#getFontData}
```
public byte[] getFontData()
```


Binary font data.

**Returns:**
byte[] - The corresponding byte[] value.
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
### getType() {#getType}
```
public int getType()
```


Returns the type of the font source.

**Returns:**
int - The type of the font source. The returned value is one of [FontSourceType](../../com.aspose.words/fontsourcetype/) constants.
### getWarningCallback() {#getWarningCallback}
```
public IWarningCallback getWarningCallback()
```


Called during processing of font source when an issue is detected that might result in formatting fidelity loss.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback/) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value.
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
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback/) | The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback/) value. |

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

