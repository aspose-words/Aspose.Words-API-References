---
title: Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings method
linktitle: LoadNotoFallbackSettings
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings method. Loads predefined fallback settings which uses Google Noto fonts in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings::LoadNotoFallbackSettings method


Loads predefined fallback settings which uses Google Noto fonts.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings()
```


## Examples



Shows how to add predefined font fallback settings for Google Noto fonts. 
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();

// These are free fonts licensed under the SIL Open Font License.
// We can download the fonts here:
// https://www.google.com/get/noto/#sans-lgc
fontSettings->SetFontsFolder(get_FontsDir() + u"Noto", false);

// Note that the predefined settings only use Sans-style Noto fonts with regular weight.
// Some of the Noto fonts use advanced typography features.
// Fonts featuring advanced typography may not be rendered correctly as Aspose.Words currently do not support them.
fontSettings->get_FallbackSettings()->LoadNotoFallbackSettings();
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(false);
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Noto Sans");

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(fontSettings);
```


Shows how to load pre-defined fallback font settings. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// Save the default fallback font scheme to an XML document.
// For example, one of the elements has a value of "0C00-0C7F" for Range and a corresponding "Vani" value for FallbackFonts.
// This means that if the font some text is using does not have symbols for the 0x0C00-0x0C7F Unicode block,
// the fallback scheme will use symbols from the "Vani" font substitute.
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.Default.xml");

// Below are two pre-defined font fallback schemes we can choose from.
// 1 -  Use the default Microsoft Office scheme, which is the same one as the default:
fontFallbackSettings->LoadMsOfficeFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 -  Use the scheme built from Google Noto fonts:
fontFallbackSettings->LoadNotoFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

## See Also

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
