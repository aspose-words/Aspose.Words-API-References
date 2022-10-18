---
title: FileFontSource
second_title: Aspose.Words for Java API Reference
description: Represents the single TrueType font file stored in the file system.
type: docs
weight: 264
url: /java/com.aspose.words/filefontsource/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase)
```
public class FileFontSource extends FontSourceBase
```

Represents the single TrueType font file stored in the file system.

To learn more, visit the **Working with Fonts** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [FileFontSource(String filePath)](#FileFontSource-java.lang.String-) | Ctor. |
| [FileFontSource(String filePath, int priority)](#FileFontSource-java.lang.String-int-) | Ctor. |
| [FileFontSource(String filePath, int priority, String cacheKey)](#FileFontSource-java.lang.String-int-java.lang.String-) | Ctor. |
## Methods

| Method | Description |
| --- | --- |
| [getFilePath()](#getFilePath--) | Path to the font file. |
| [getCacheKey()](#getCacheKey--) | The key of this source in the cache. |
| [getType()](#getType--) | Returns the type of the font source. |
| [getFontDataInternal()](#getFontDataInternal--) |  |
### FileFontSource(String filePath) {#FileFontSource-java.lang.String-}
```
public FileFontSource(String filePath)
```


Ctor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| filePath | java.lang.String | Path to font file. |

### FileFontSource(String filePath, int priority) {#FileFontSource-java.lang.String-int-}
```
public FileFontSource(String filePath, int priority)
```


Ctor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| filePath | java.lang.String | Path to font file. |
| priority | int | Font source priority. See the [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase\#getPriority--) property description for more information. |

### FileFontSource(String filePath, int priority, String cacheKey) {#FileFontSource-java.lang.String-int-java.lang.String-}
```
public FileFontSource(String filePath, int priority, String cacheKey)
```


Ctor.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| filePath | java.lang.String | Path to font file. |
| priority | int | Font source priority. See the [FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase\#getPriority--) property description for more information. |
| cacheKey | java.lang.String | The key of this source in the cache. See [getCacheKey()](../../com.aspose.words/filefontsource\#getCacheKey--) property description for more information. |

### getFilePath() {#getFilePath--}
```
public String getFilePath()
```


Path to the font file.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### getCacheKey() {#getCacheKey--}
```
public String getCacheKey()
```


The key of this source in the cache.

This key is used to identify cache item when saving/loading font search cache with  and  methods.

If key is not specified then [getFilePath()](../../com.aspose.words/filefontsource\#getFilePath--) will be used as a key instead.

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
