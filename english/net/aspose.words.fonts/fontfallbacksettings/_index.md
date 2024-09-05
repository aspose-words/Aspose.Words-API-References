---
title: FontFallbackSettings Class
linktitle: FontFallbackSettings
articleTitle: FontFallbackSettings
second_title: Aspose.Words for .NET
description: Aspose.Words.Fonts.FontFallbackSettings class. Specifies font fallback mechanism settings in C#.
type: docs
weight: 3180
url: /net/aspose.words.fonts/fontfallbacksettings/
---
## FontFallbackSettings class

Specifies font fallback mechanism settings.

To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/net/working-with-fonts/) documentation article.

```csharp
public class FontFallbackSettings
```

## Methods

| Name | Description |
| --- | --- |
| [BuildAutomatic](../../aspose.words.fonts/fontfallbacksettings/buildautomatic/)() | Automatically builds the fallback settings by scanning available fonts. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load)(*Stream*) | Loads fallback settings from XML stream. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load_1)(*string*) | Loads font fallback settings from XML file. |
| [LoadMsOfficeFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/)() | Loads predefined fallback settings which mimics the Microsoft Word fallback and uses Microsoft office fonts. |
| [LoadNotoFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/)() | Loads predefined fallback settings which uses Google Noto fonts. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save)(*Stream*) | Saves the current fallback settings to stream. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save_1)(*string*) | Saves the current fallback settings to file. |

## Remarks

By default fallback settings are initialized with predefined settings which mimics the Microsoft Word fallback.

## Examples

Shows how to distribute fallback fonts across Unicode character code ranges.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Configure our font settings to source fonts only from the "MyFonts" folder.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Calling the "BuildAutomatic" method will generate a fallback scheme that
// distributes accessible fonts across as many Unicode character codes as possible.
// In our case, it only has access to the handful of fonts inside the "MyFonts" folder.
fontFallbackSettings.BuildAutomatic();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// We can also load a custom substitution scheme from a file like this.
// This scheme applies the "AllegroOpen" font across the "0000-00ff" Unicode blocks, the "AllegroOpen" font across "0100-024f",
// and the "M+ 2m" font in all other ranges that other fonts in the scheme do not cover.
fontFallbackSettings.Load(MyDir + "Custom font fallback settings.xml");

// Create a document builder and set its font to one that does not exist in any of our sources.
// Our font settings will invoke the fallback scheme for characters that we type using the unavailable font.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Missing Font";

// Use the builder to print every Unicode character from 0x0021 to 0x052F,
// with descriptive lines dividing Unicode blocks we defined in our custom font fallback scheme.
for (int i = 0x0021; i < 0x0530; i++)
{
    switch (i)
    {
        case 0x0021:
            builder.Writeln(
                "\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in \"AllegroOpen\" font:");
            break;
        case 0x0100:
            builder.Writeln(
                "\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in \"AllegroOpen\" font:");
            break;
        case 0x0250:
            builder.Writeln("\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in \"M+ 2m\" font:");
            break;
    }

    builder.Write($"{Convert.ToChar(i)}");
}

doc.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.pdf");
```

### See Also

* namespace [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assembly [Aspose.Words](../../)
