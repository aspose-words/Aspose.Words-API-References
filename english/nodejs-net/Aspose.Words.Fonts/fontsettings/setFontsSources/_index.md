---
title: FontSettings.setFontsSources method
linktitle: setFontsSources method
articleTitle: setFontsSources method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Fonts.FontSettings.setFontsSources method"
type: docs
weight: 100
url: /nodejs-net/aspose.words.fonts/fontsettings/setFontsSources/
---

## setFontsSources(sources) {#fontsourcebase[]}

Sets the sources where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts.


```js
setFontsSources(sources: Aspose.Words.Fonts.FontSourceBase[])
```

| Parameter | Type | Description |
| --- | --- | --- |
| sources | [FontSourceBase](../../fontsourcebase/)[] | An array of sources that contain TrueType fonts. |

### Remarks

By default, Aspose.Words looks for fonts installed to the system.

Setting this property resets the cache of all previously loaded fonts.




## setFontsSources(sources, cacheInputStream) {#fontsourcebase[]_buffer}

Sets the sources where Aspose.Words looks for TrueType fonts and additionally loads previously saved
font search cache.


```js
setFontsSources(sources: Aspose.Words.Fonts.FontSourceBase[], cacheInputStream: Buffer)
```

| Parameter | Type | Description |
| --- | --- | --- |
| sources | [FontSourceBase](../../fontsourcebase/)[] | An array of sources that contain TrueType fonts. |
| cacheInputStream | Buffer | Input stream with saved font search cache. |

### Remarks

Loading previously saved font search cache will speed up the font cache initialization process. It is
especially useful when access to font sources is complicated (e.g. when fonts are loaded via network).

When saving and loading font search cache, fonts in the provided sources are identified via cache key.
For the fonts in the [SystemFontSource](../../systemfontsource/) and [FolderFontSource](../../folderfontsource/) cache key is the path
to the font file. For [MemoryFontSource](../../memoryfontsource/) and [StreamFontSource](../../streamfontsource/) cache key is defined
in the [MemoryFontSource.cacheKey](../../memoryfontsource/cacheKey/) and [StreamFontSource.cacheKey](../../streamfontsource/cacheKey/) properties
respectively. For the [FileFontSource](../../filefontsource/) cache key is either [FileFontSource.cacheKey](../../filefontsource/cacheKey/)
property or a file path if the [FileFontSource.cacheKey](../../filefontsource/cacheKey/) is ``null``.

It is highly recommended to provide the same font sources when loading cache as at the time the cache was saved.
Any changes in the font sources (e.g. adding new fonts, moving font files or changing the cache key) may lead to the
inaccurate font resolving by Aspose.Words.




## See Also

* module [Aspose.Words.Fonts](../../)
* class [FontSettings](../)

