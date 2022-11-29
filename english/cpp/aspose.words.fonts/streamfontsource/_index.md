---
title: StreamFontSource
second_title: Aspose.Words for C++ API Reference
description: Base class for user-defined stream font source.
type: docs
weight: 196
url: /cpp/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class


Base class for user-defined stream font source.

```cpp
class StreamFontSource : public Aspose::Words::Fonts::FontSourceBase,
                         public Aspose::Fonts::IFontData
```

## Methods

| Method | Description |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | The key of this source in the cache. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Returns the font source priority. |
| [get_Type](./get_type/)() override | Returns the type of the font source. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Returns list of fonts available via this source. |
| virtual [OpenFontDataStream](./openfontdatastream/)() | This method should open the stream with font data on demand. |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Setter for [Aspose::Words::Fonts::FontSourceBase::get_WarningCallback](../fontsourcebase/get_warningcallback/). |
## Remarks


In order to use the stream font source you should create a derived class from the [StreamFontSource](./) and provide implementation of the [OpenFontDataStream](./openfontdatastream/) method.

[OpenFontDataStream](./openfontdatastream/) method could be called several times. For the first time it will be called when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the font is used in the document to parse the font data and to embed the font data to some output formats.

[StreamFontSource](./) may be useful because it allows to load the font data only when it is required and not to store it in the memory for the [FontSettings](../fontsettings/) lifetime.

## Examples



Shows how to load fonts from stream. 
```cpp
void StreamFontSourceFileRendering()
{
    auto fontSettings = MakeObject<FontSettings>();
    fontSettings->SetFontsSources(MakeArray<SharedPtr<FontSourceBase>>({MakeObject<ExFontSettings::StreamFontSourceFile>()}));

    auto builder = MakeObject<DocumentBuilder>();
    builder->get_Document()->set_FontSettings(fontSettings);
    builder->get_Font()->set_Name(u"Kreon-Regular");
    builder->Writeln(u"Test aspose text when saving to PDF.");

    builder->get_Document()->Save(ArtifactsDir + u"FontSettings.StreamFontSourceFileRendering.pdf");
}

class StreamFontSourceFile : public StreamFontSource
{
public:
    SharedPtr<System::IO::Stream> OpenFontDataStream() override
    {
        return System::IO::File::OpenRead(FontsDir + u"Kreon-Regular.ttf");
    }

protected:
    virtual ~StreamFontSourceFile()
    {
    }
};
```

## See Also

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words](../../)
