---
title: FileFontSource.CacheKey
linktitle: CacheKey
articleTitle: CacheKey
second_title: Aspose.Words for .NET API Reference
description: FileFontSource CacheKey property. The key of this source in the cache in C#.
type: docs
weight: 20
url: /net/aspose.words.fonts/filefontsource/cachekey/
---
## FileFontSource.CacheKey property

The key of this source in the cache.

```csharp
public string CacheKey { get; }
```

## Remarks

This key is used to identify cache item when saving/loading font search cache with [`SaveSearchCache`](../../fontsettings/savesearchcache/) and [`SetFontsSources`](../../fontsettings/setfontssources/) methods.

If key is not specified then [`FilePath`](../filepath/) will be used as a key instead.

### See Also

* class [FileFontSource](../)
* namespace [Aspose.Words.Fonts](../../filefontsource/)
* assembly [Aspose.Words](../../../)
