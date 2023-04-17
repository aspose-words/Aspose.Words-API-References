---
title: Aspose::Words::Fonts::StreamFontSource::OpenFontDataStream method
linktitle: OpenFontDataStream
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::StreamFontSource::OpenFontDataStream method. This method should open the stream with font data on demand in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.fonts/streamfontsource/openfontdatastream/
---
## StreamFontSource::OpenFontDataStream method


This method should open the stream with font data on demand.

```cpp
virtual System::SharedPtr<System::IO::Stream> Aspose::Words::Fonts::StreamFontSource::OpenFontDataStream()=0
```


### ReturnValue

[Font](../../../aspose.words/font/) data stream.

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

* Class [StreamFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
