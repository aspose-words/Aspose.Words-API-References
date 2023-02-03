---
title: StreamFontSource class
second_title: Aspose.Words for Python via .NET API Reference
description: "Base class for user-defined stream font source"
type: docs
weight: 210
url: /python-net/aspose.words.fonts/streamfontsource/
---

## StreamFontSource class

Base class for user-defined stream font source.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/python-net/working-with-fonts/) documentation article.




In order to use the stream font source you should create a derived class from the [StreamFontSource](./)
and provide implementation of the [StreamFontSource.open_font_data_stream()](./open_font_data_stream/#default) method.

[StreamFontSource.open_font_data_stream()](./open_font_data_stream/#default) method could be called several times. For the first time it will be called
when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the
font is used in the document to parse the font data and to embed the font data to some output formats.

[StreamFontSource](./) may be useful because it allows to load the font data only when it is required
and not to store it in the memory for the [FontSettings](../fontsettings/) lifetime.




**Inheritance:** [StreamFontSource](./) → [FontSourceBase](../fontsourcebase/)

### Properties

| Name | Description |
| --- | --- |
| [cache_key](./cache_key/) | The key of this source in the cache. |
| [priority](../fontsourcebase/priority/) | Returns the font source priority.<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |
| [type](./type/) | Returns the type of the font source. |
| [warning_callback](../fontsourcebase/warning_callback/) | Called during processing of font source when an issue is detected that might result in formatting fidelity loss.<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_available_fonts()](../fontsourcebase/get_available_fonts/#default) | Returns list of fonts available via this source.<br>(Inherited from [FontSourceBase](../fontsourcebase/)) |
|[ open_font_data_stream()](./open_font_data_stream/#default) | This method should open the stream with font data on demand. |

### See Also

* module [aspose.words.fonts](../)
* class [FontSourceBase](../fontsourcebase/)

