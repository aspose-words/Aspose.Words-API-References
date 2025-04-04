---
title: FileFontSource.cacheKey property
linktitle: cacheKey property
articleTitle: cacheKey property
second_title: Aspose.Words for Node.js
description: "FileFontSource.cacheKey property. The key of this source in the cache."
type: docs
weight: 20
url: /nodejs-net/aspose.words.fonts/filefontsource/cacheKey/
---

## FileFontSource.cacheKey property

The key of this source in the cache.


```js
get cacheKey(): string
```

### Remarks

This key is used to identify cache item when saving/loading font search cache with
[FontSettings.saveSearchCache()](../../fontsettings/saveSearchCache/#buffer) and
[FontSettings.setFontsSources()](../../fontsettings/setFontsSources/#fontsourcebase[]_buffer) methods.

If key is not specified then [FileFontSource.filePath](../filePath/) will be used as a key instead.




### See Also

* module [Aspose.Words.Fonts](../../)
* class [FileFontSource](../)

