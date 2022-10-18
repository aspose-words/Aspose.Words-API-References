---
title: MemoryFontSource
second_title: Aspose.Words for Java API Reference
description: Represents the single TrueType font file stored in memory.
type: docs
weight: 393
url: /java/com.aspose.words/memoryfontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase)
```
public class MemoryFontSource extends FontSourceBase
```

Represents the single TrueType font file stored in memory.

To learn more, visit the **Working with Fonts** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [MemoryFontSource(byte[] fontData)](#MemoryFontSource-byte---) | Ctor. |
| [MemoryFontSource(byte[] fontData, int priority)](#MemoryFontSource-byte---int-) | Ctor. |
| [MemoryFontSource(byte[] fontData, int priority, String cacheKey)](#MemoryFontSource-byte---int-java.lang.String-) | Ctor. |
## Methods

| Method | Description |
| --- | --- |
| [getFontData()](#getFontData--) | Binary font data. |
| [getCacheKey()](#getCacheKey--) | The key of this source in the cache. |
| [getType()](#getType--) | Returns the type of the font source. |
| [getFontDataInternal()](#getFontDataInternal--) |  |
### MemoryFontSource(byte[] fontData) {#MemoryFontSource-byte---}
```
public MemoryFontSource(byte[] fontData)
```


Ctor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontData | byte[] | Binary font data. |

### MemoryFontSource(byte[] fontData, int priority) {#MemoryFontSource-byte---int-}
```
public MemoryFontSource(byte[] fontData, int priority)
```


Ctor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontData | byte[] | Binary font data. |
| priority | int | Font source priority. See the [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase\#getPriority--) property description for more information. |

### MemoryFontSource(byte[] fontData, int priority, String cacheKey) {#MemoryFontSource-byte---int-java.lang.String-}
```
public MemoryFontSource(byte[] fontData, int priority, String cacheKey)
```


Ctor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fontData | byte[] | Binary font data. |
| priority | int | Font source priority. See the [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase\#getPriority--) property description for more information. |
| cacheKey | java.lang.String | The key of this source in the cache. See [getCacheKey()](../../com.aspose.words/memoryfontsource\#getCacheKey--) property description for more information. |

### getFontData() {#getFontData--}
```
public byte[] getFontData()
```


Binary font data.

**Returns:**
byte[] - The corresponding byte[] value.
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
### getFontDataInternal() {#getFontDataInternal--}
```
public Iterable getFontDataInternal()
```




**Returns:**
java.lang.Iterable
