---
title: FontSettings.FallbackSettings
linktitle: FallbackSettings
articleTitle: FallbackSettings
second_title: Aspose.Words for .NET
description: Discover the FontSettings FallbackSettings property for optimized font fallback mechanisms. Enhance your design with seamless text rendering!
type: docs
weight: 30
url: /net/aspose.words.fonts/fontsettings/fallbacksettings/
---
## FontSettings.FallbackSettings property

Settings related to font fallback mechanism.

```csharp
public FontFallbackSettings FallbackSettings { get; }
```

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

* class [FontFallbackSettings](../../fontfallbacksettings/)
* class [FontSettings](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
