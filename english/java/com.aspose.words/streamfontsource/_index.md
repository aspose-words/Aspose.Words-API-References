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
| [getCacheKey()](#getCacheKey--) | The key of this source in the cache. |
| [getType()](#getType--) | Returns the type of the font source. |
| [openFontDataStream()](#openFontDataStream--) | This method should open the stream with font data on demand. |
| [getSize()](#getSize--) |  |
| [getFilePath()](#getFilePath--) |  |
| [getCacheKeyInternal()](#getCacheKeyInternal--) |  |
| [getFontDataInternal()](#getFontDataInternal--) |  |
### getCacheKey() {#getCacheKey--}
```
public String getCacheKey()
```


The key of this source in the cache. This key is used to identify cache item when saving/loading font search cache with  and  methods.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getType() {#getType--}
```
public int getType()
```


Returns the type of the font source.

**Returns:**
int - The type of the font source. The returned value is one of [FontSourceType](../../com.aspose.words/fontsourcetype) constants.
### openFontDataStream() {#openFontDataStream--}
```
public abstract InputStream openFontDataStream()
```


This method should open the stream with font data on demand.

**Returns:**
java.io.InputStream - Font data stream. The stream will be closed after reading. There is no need to close it explicitly.
### getSize() {#getSize--}
```
public int getSize()
```




**Returns:**
int
### getFilePath() {#getFilePath--}
```
public String getFilePath()
```




**Returns:**
java.lang.String
### getCacheKeyInternal() {#getCacheKeyInternal--}
```
public String getCacheKeyInternal()
```




**Returns:**
java.lang.String
### getFontDataInternal() {#getFontDataInternal--}
```
public Iterable getFontDataInternal()
```




**Returns:**
java.lang.Iterable
