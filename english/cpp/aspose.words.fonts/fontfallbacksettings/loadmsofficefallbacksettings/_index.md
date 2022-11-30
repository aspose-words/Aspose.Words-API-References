---
title: LoadMsOfficeFallbackSettings
second_title: Aspose.Words for C++ API Reference
description: Loads predefined fallback settings which mimics the Microsoft Word fallback and uses Microsoft office fonts.
type: docs
weight: 27
url: /cpp/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings::LoadMsOfficeFallbackSettings method


Loads predefined fallback settings which mimics the Microsoft Word fallback and uses Microsoft office fonts.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings()
```


## Examples



Shows how to load pre-defined fallback font settings. 
```cpp
auto doc = MakeObject<Document>();

auto fontSettings = MakeObject<FontSettings>();
doc->set_FontSettings(fontSettings);
SharedPtr<FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// Save the default fallback font scheme to an XML document.
// For example, one of the elements has a value of "0C00-0C7F" for Range and a corresponding "Vani" value for FallbackFonts.
// This means that if the font some text is using does not have symbols for the 0x0C00-0x0C7F Unicode block,
// the fallback scheme will use symbols from the "Vani" font substitute.
fontFallbackSettings->Save(ArtifactsDir + u"FontSettings.FallbackSettings.Default.xml");

// Below are two pre-defined font fallback schemes we can choose from.
// 1 -  Use the default Microsoft Office scheme, which is the same one as the default:
fontFallbackSettings->LoadMsOfficeFallbackSettings();
fontFallbackSettings->Save(ArtifactsDir + u"FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 -  Use the scheme built from Google Noto fonts:
fontFallbackSettings->LoadNotoFallbackSettings();
fontFallbackSettings->Save(ArtifactsDir + u"FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

## See Also

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words](../../../)
