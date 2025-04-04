---
title: FontSettings class
linktitle: FontSettings class
articleTitle: FontSettings class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Fonts.FontSettings class. Specifies font settings for a document"
type: docs
weight: 160
url: /nodejs-net/aspose.words.fonts/fontsettings/
---

## FontSettings class

Specifies font settings for a document.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/nodejs-net/working-with-fonts/) documentation article.




### Remarks

Aspose.Words uses font settings to resolve the fonts in the document. Fonts are resolved mostly when building document layout
or rendering to fixed page formats. But when loading some formats, Aspose.Words also may require to resolve the fonts. For example, when
loading HTML documents Aspose.Words may resolve the fonts to perform font fallback. So it is recommended that you set the font settings in
[LoadOptions](../../aspose.words.loading/loadoptions/) when loading the document. Or at least before building the layout or rendering the document to the fixed-page format.

By default all documents uses single static font settings instance. It could be accessed by
[FontSettings.defaultInstance](./defaultInstance/) property.

Changing font settings is safe at any time from any thread. But it is recommended that you do not change the font settings while
processing some documents which uses this settings. This can lead to the fact that the same font will be resolved differently
in different parts of the document.




### Constructors
| Name | Description |
| --- | --- |
| [FontSettings()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [defaultInstance](./defaultInstance/) | Static default font settings. |
| [fallbackSettings](./fallbackSettings/) | Settings related to font fallback mechanism. |
| [substitutionSettings](./substitutionSettings/) | Settings related to font substitution mechanism. |

### Methods

| Name | Description |
| --- | --- |
|[ getFontsSources()](./getFontsSources/#default) | Gets a copy of the array that contains the list of sources where Aspose.Words looks for TrueType fonts. |
|[ resetFontSources()](./resetFontSources/#default) | Resets the fonts sources to the system default. |
|[ saveSearchCache(outputStream)](./saveSearchCache/#buffer) | Saves the font search cache to the stream. |
|[ setFontsFolder(fontFolder, recursive)](./setFontsFolder/#string_boolean) | Sets the folder where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. This is a shortcut to [FontSettings.setFontsFolders()](./setFontsFolders/#string[]_boolean) for setting only one font directory. |
|[ setFontsFolders(fontsFolders, recursive)](./setFontsFolders/#string[]_boolean) | Sets the folders where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. |
|[ setFontsSources(sources)](./setFontsSources/#fontsourcebase[]) | Sets the sources where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. |
|[ setFontsSources(sources, cacheInputStream)](./setFontsSources/#fontsourcebase[]_buffer) | Sets the sources where Aspose.Words looks for TrueType fonts and additionally loads previously saved font search cache. |

### See Also

* module [Aspose.Words.Fonts](../)

