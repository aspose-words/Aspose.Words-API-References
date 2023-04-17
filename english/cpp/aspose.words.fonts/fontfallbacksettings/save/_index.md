---
title: Aspose::Words::Fonts::FontFallbackSettings::Save method
linktitle: Save
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontFallbackSettings::Save method. Saves the current fallback settings to stream in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.fonts/fontfallbacksettings/save/
---
## FontFallbackSettings::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


Saves the current fallback settings to stream.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Save(const System::SharedPtr<System::IO::Stream> &outputStream)
```


| Parameter | Type | Description |
| --- | --- | --- |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Output stream. |

## Examples



Shows how to load and save font fallback settings to/from a stream. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

// Load an XML document that defines a set of font fallback settings.
{
    auto fontFallbackStream = MakeObject<System::IO::FileStream>(MyDir + u"Font fallback rules.xml", System::IO::FileMode::Open);
    auto fontSettings = MakeObject<FontSettings>();
    fontSettings->get_FallbackSettings()->Load(fontFallbackStream);

    doc->set_FontSettings(fontSettings);
}

doc->Save(ArtifactsDir + u"FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// Use a stream to save our document's current font fallback settings as an XML document.
{
    auto fontFallbackStream = MakeObject<System::IO::FileStream>(ArtifactsDir + u"FallbackSettings.xml", System::IO::FileMode::Create);
    doc->get_FontSettings()->get_FallbackSettings()->Save(fontFallbackStream);
}
```

## See Also

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontFallbackSettings::Save(const System::String\&) method


Saves the current fallback settings to file.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Save(const System::String &fileName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Output file name. |

## Examples



Shows how to load and save font fallback settings to/from an XML document in the local file system. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

// Load an XML document that defines a set of font fallback settings.
auto fontSettings = MakeObject<FontSettings>();
fontSettings->get_FallbackSettings()->Load(MyDir + u"Font fallback rules.xml");

doc->set_FontSettings(fontSettings);
doc->Save(ArtifactsDir + u"FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Save our document's current font fallback settings as an XML document.
doc->get_FontSettings()->get_FallbackSettings()->Save(ArtifactsDir + u"FallbackSettings.xml");
```

## See Also

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontFallbackSettings::Save(std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Fonts::FontFallbackSettings::Save(std::basic_ostream<CharType, Traits> &outputStream)
```

## See Also

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
