---
title: Aspose::Words::Fonts::FontFallbackSettings class
linktitle: FontFallbackSettings
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontFallbackSettings class. Specifies font fallback mechanism settings. To learn more, visit the  documentation article in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.fonts/fontfallbacksettings/
---
## FontFallbackSettings class


Specifies font fallback mechanism settings. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FontFallbackSettings : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [BuildAutomatic](./buildautomatic/)() | Automatically builds the fallback settings by scanning available fonts. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Load](./load/)(const System::String\&) | Loads font fallback settings from XML file. |
| [Load](./load/)(const System::SharedPtr\<System::IO::Stream\>\&) | Loads fallback settings from XML stream. |
| [Load](./load/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [LoadMsOfficeFallbackSettings](./loadmsofficefallbacksettings/)() | Loads predefined fallback settings which mimics the Microsoft Word fallback and uses Microsoft office fonts. |
| [LoadNotoFallbackSettings](./loadnotofallbacksettings/)() | Loads predefined fallback settings which uses Google Noto fonts. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Saves the current fallback settings to stream. |
| [Save](./save/)(const System::String\&) | Saves the current fallback settings to file. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |

## Examples



Shows how to distribute fallback fonts across Unicode character code ranges. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// Configure our font settings to source fonts only from the "MyFonts" folder.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// Calling the "BuildAutomatic" method will generate a fallback scheme that
// distributes accessible fonts across as many Unicode character codes as possible.
// In our case, it only has access to the handful of fonts inside the "MyFonts" folder.
fontFallbackSettings->BuildAutomatic();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// We can also load a custom substitution scheme from a file like this.
// This scheme applies the "AllegroOpen" font across the "0000-00ff" Unicode blocks, the "AllegroOpen" font across "0100-024f",
// and the "M+ 2m" font in all other ranges that other fonts in the scheme do not cover.
fontFallbackSettings->Load(get_MyDir() + u"Custom font fallback settings.xml");

// Create a document builder and set its font to one that does not exist in any of our sources.
// Our font settings will invoke the fallback scheme for characters that we type using the unavailable font.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Missing Font");

// Use the builder to print every Unicode character from 0x0021 to 0x052F,
// with descriptive lines dividing Unicode blocks we defined in our custom font fallback scheme.
for (int32_t i = 0x0021; i < 0x0530; i++)
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

    builder->Write(System::String::Format(u"{0}", System::Convert::ToChar(i)));
}

doc->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettingsCustom.pdf");
```

## See Also

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
