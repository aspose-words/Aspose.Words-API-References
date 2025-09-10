---
title: StreamFontSource class
linktitle: StreamFontSource class
articleTitle: StreamFontSource class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Fonts.StreamFontSource class. Base class for user-defined stream font source"
type: docs
weight: 230
url: /nodejs-net/aspose.words.fonts/streamfontsource/
---

## StreamFontSource class

Base class for user-defined stream font source.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/nodejs-net/working-with-fonts/) documentation article.




### Remarks

In order to use the stream font source you should create a derived class from the [StreamFontSource](./)
and provide implementation of the Aspose.Words.Fonts.StreamFontSource.OpenFontDataStream method.

Aspose.Words.Fonts.StreamFontSource.OpenFontDataStream method could be called several times. For the first time it will be called
when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the
font is used in the document to parse the font data and to embed the font data to some output formats.

[StreamFontSource](./) may be useful because it allows to load the font data only when it is required
and not to store it in the memory for the [FontSettings](../fontsettings/) lifetime.




**Inheritance:** [StreamFontSource](./) → [FontSourceBase](../fontsourcebase/)

### Properties

| Name | Description |
| --- | --- |
| [cacheKey](./cacheKey/) | The key of this source in the cache. |
| [isEmbedded](./isEmbedded/) |  |
| [priority](../fontsourcebase/priority/) | Returns the font source priority.<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |
| [type](./type/) | Returns the type of the font source. |

### Methods

| Name | Description |
| --- | --- |
|[ asFileFontSource()](../fontsourcebase/asFileFontSource/#default) | Cast [FontSourceBase](../fontsourcebase/) object to [FileFontSource](../filefontsource/).<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |
|[ asFolderFontSource()](../fontsourcebase/asFolderFontSource/#default) | Cast [FontSourceBase](../fontsourcebase/) object to [FolderFontSource](../folderfontsource/).<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |
|[ asMemoryFontSource()](../fontsourcebase/asMemoryFontSource/#default) | Cast [FontSourceBase](../fontsourcebase/) object to [MemoryFontSource](../memoryfontsource/).<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |
|[ asStreamFontSource()](../fontsourcebase/asStreamFontSource/#default) | Cast [FontSourceBase](../fontsourcebase/) object to [StreamFontSource](./).<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |
|[ asSystemFontSource()](../fontsourcebase/asSystemFontSource/#default) | Cast [FontSourceBase](../fontsourcebase/) object to [SystemFontSource](../systemfontsource/).<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |

### See Also

* module [Aspose.Words.Fonts](../)
* class [FontSourceBase](../fontsourcebase/)

