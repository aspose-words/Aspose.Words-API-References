---
title: StreamFontSource
second_title: Aspose.Words for Java API Reference
description: Base class for user-defined stream font source.
type: docs
weight: 530
url: /java/com.aspose.words/streamfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase)
```
public abstract class StreamFontSource extends FontSourceBase
```

Base class for user-defined stream font source.

To learn more, visit the **Working with Fonts** documentation article.

In order to use the stream font source you should create a derived class from the [StreamFontSource](../../com.aspose.words/streamfontsource) and provide implementation of the [openFontDataStream()](../../com.aspose.words/streamfontsource\#openFontDataStream--) method.

[openFontDataStream()](../../com.aspose.words/streamfontsource\#openFontDataStream--) method could be called several times. For the first time it will be called when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the font is used in the document to parse the font data and to embed the font data to some output formats.

[StreamFontSource](../../com.aspose.words/streamfontsource) may be useful because it allows to load the font data only when it is required and not to store it in the memory for the [FontSettings](../../com.aspose.words/fontsettings) lifetime.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAvailableFonts()](#getAvailableFonts--) | Returns list of fonts available via this source. |
| [getCacheKey()](#getCacheKey--) | The key of this source in the cache. |
| [getCacheKeyInternal()](#getCacheKeyInternal--) |  |
| [getClass()](#getClass--) |  |
| [getFilePath()](#getFilePath--) |  |
| [getFontDataInternal()](#getFontDataInternal--) |  |
| [getPriority()](#getPriority--) | Returns the font source priority. |
| [getPriorityInternal()](#getPriorityInternal--) |  |
| [getSize()](#getSize--) |  |
| [getType()](#getType--) | Returns the type of the font source. |
| [getWarningCallback()](#getWarningCallback--) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [openFontDataStream()](#openFontDataStream--) | This method should open the stream with font data on demand. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getAvailableFonts() {#getAvailableFonts--}
```
public ArrayList getAvailableFonts()
```


Returns list of fonts available via this source.

**Returns:**
java.util.ArrayList
### getCacheKey() {#getCacheKey--}
```
public String getCacheKey()
```


The key of this source in the cache. This key is used to identify cache item when saving/loading font search cache with  and  methods.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getCacheKeyInternal() {#getCacheKeyInternal--}
```
public String getCacheKeyInternal()
```




**Returns:**
java.lang.String
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getFilePath() {#getFilePath--}
```
public String getFilePath()
```




**Returns:**
java.lang.String
### getFontDataInternal() {#getFontDataInternal--}
```
public Iterable getFontDataInternal()
```




**Returns:**
java.lang.Iterable
### getPriority() {#getPriority--}
```
public int getPriority()
```


Returns the font source priority.

This value is used when there are fonts with the same family name and style in different font sources. In this case Aspose.Words selects the font from the source with the higher priority value.

The default value is 0.

**Returns:**
int - The font source priority.
### getPriorityInternal() {#getPriorityInternal--}
```
public int getPriorityInternal()
```




**Returns:**
int
### getSize() {#getSize--}
```
public int getSize()
```




**Returns:**
int
### getType() {#getType--}
```
public int getType()
```


Returns the type of the font source.

**Returns:**
int - The type of the font source. The returned value is one of [FontSourceType](../../com.aspose.words/fontsourcetype) constants.
### getWarningCallback() {#getWarningCallback--}
```
public IWarningCallback getWarningCallback()
```


Called during processing of font source when an issue is detected that might result in formatting fidelity loss.

**Returns:**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback) value.
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




### openFontDataStream() {#openFontDataStream--}
```
public abstract InputStream openFontDataStream()
```


This method should open the stream with font data on demand.

**Returns:**
java.io.InputStream - Font data stream. The stream will be closed after reading. There is no need to close it explicitly.
### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public void setWarningCallback(IWarningCallback value)
```


Called during processing of font source when an issue is detected that might result in formatting fidelity loss.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback) | The corresponding [IWarningCallback](../../com.aspose.words/iwarningcallback) value. |

### toString() {#toString--}
```
public String toString()
```




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

