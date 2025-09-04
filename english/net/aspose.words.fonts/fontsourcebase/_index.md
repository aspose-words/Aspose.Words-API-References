---
title: FontSourceBase Class
linktitle: FontSourceBase
articleTitle: FontSourceBase
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Fonts.FontSourceBase, the essential abstract class for defining diverse font sources in your applications. Enhance your document formatting!
type: docs
weight: 3420
url: /net/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class

This is an abstract base class for the classes that allow the user to specify various font sources.

To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/net/working-with-fonts/) documentation article.

```csharp
public abstract class FontSourceBase
```

## Properties

| Name | Description |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Returns the font source priority. |
| abstract [Type](../../aspose.words.fonts/fontsourcebase/type/) { get; } | Returns the type of the font source. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |

## Methods

| Name | Description |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Returns list of fonts available via this source. |

## Examples

Shows how to use a font file in the local file system as a font source.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.That(fileFontSource.FilePath, Is.EqualTo(MyDir + "Alte DIN 1451 Mittelschrift.ttf"));
Assert.That(fileFontSource.Type, Is.EqualTo(FontSourceType.FontFile));
Assert.That(fileFontSource.Priority, Is.EqualTo(0));
```

### See Also

* namespace [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assembly [Aspose.Words](../../)
