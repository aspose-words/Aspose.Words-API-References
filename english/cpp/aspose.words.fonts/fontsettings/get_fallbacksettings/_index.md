---
title: get_FallbackSettings
second_title: Aspose.Words for C++ API Reference
description: Settings related to font fallback mechanism.
type: docs
weight: 40
url: /cpp/aspose.words.fonts/fontsettings/get_fallbacksettings/
---
## FontSettings::get_FallbackSettings method


[Settings](../../../aspose.words.settings/) related to font fallback mechanism.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> Aspose::Words::Fonts::FontSettings::get_FallbackSettings() const
```


## Examples



Shows how to distribute fallback fonts across Unicode character code ranges. 
```cpp
auto doc = MakeObject<Document>();

auto fontSettings = MakeObject<FontSettings>();
doc->set_FontSettings(fontSettings);
SharedPtr<FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// Configure our font settings to source fonts only from the "MyFonts" folder.
auto folderFontSource = MakeObject<FolderFontSource>(FontsDir, false);
fontSettings->SetFontsSources(MakeArray<SharedPtr<FontSourceBase>>({folderFontSource}));

// Calling the "BuildAutomatic" method will generate a fallback scheme that
// distributes accessible fonts across as many Unicode character codes as possible.
// In our case, it only has access to the handful of fonts inside the "MyFonts" folder.
fontFallbackSettings->BuildAutomatic();
fontFallbackSettings->Save(ArtifactsDir + u"FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// We can also load a custom substitution scheme from a file like this.
// This scheme applies the "AllegroOpen" font across the "0000-00ff" Unicode blocks, the "AllegroOpen" font across "0100-024f",
// and the "M+ 2m" font in all other ranges that other fonts in the scheme do not cover.
fontFallbackSettings->Load(MyDir + u"Custom font fallback settings.xml");

// Create a document builder and set its font to one that does not exist in any of our sources.
// Our font settings will invoke the fallback scheme for characters that we type using the unavailable font.
auto builder = MakeObject<DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Missing Font");

// Use the builder to print every Unicode character from 0x0021 to 0x052F,
// with descriptive lines dividing Unicode blocks we defined in our custom font fallback scheme.
for (int i = 0x0021; i < 0x0530; i++)
{
    switch (i)
    {
    case 0x0021:
        builder->Writeln(u"\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in \"AllegroOpen\" font:");
        break;

    case 0x0100:
        builder->Writeln(u"\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in \"AllegroOpen\" font:");
        break;

    case 0x0250:
        builder->Writeln(u"\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in \"M+ 2m\" font:");
        break;
    }

    builder->Write(String::Format(u"{0}", System::Convert::ToChar(i)));
}

doc->Save(ArtifactsDir + u"FontSettings.FallbackSettingsCustom.pdf");
```

## See Also

* Class [FontFallbackSettings](../../fontfallbacksettings/)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words](../../../)
