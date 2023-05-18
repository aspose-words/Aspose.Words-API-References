---
title: Aspose::Words::Fonts::FontSettings::get_DefaultInstance method
linktitle: get_DefaultInstance
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontSettings::get_DefaultInstance method. Static default font settings in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.fonts/fontsettings/get_defaultinstance/
---
## FontSettings::get_DefaultInstance method


Static default font settings.

```cpp
static System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Fonts::FontSettings::get_DefaultInstance()
```


## Examples



Shows how to configure the default font settings instance. 
```cpp
// Configure the default font settings instance to use the "Courier New" font
// as a backup substitute when we attempt to use an unknown font.
FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Courier New");

ASSERT_TRUE(FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->get_Enabled());

auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

// This document does not have a FontSettings configuration. When we render the document,
// the default FontSettings instance will resolve the missing font.
// Aspose.Words will use "Courier New" to render text that uses the unknown font.
ASSERT_TRUE(doc->get_FontSettings() == nullptr);

doc->Save(ArtifactsDir + u"FontSettings.DefaultFontInstance.pdf");
```


Shows how to use the [IWarningCallback](../../../aspose.words/iwarningcallback/) interface to monitor font substitution warnings. 
```cpp
void SubstitutionWarning()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    builder->get_Font()->set_Name(u"Times New Roman");
    builder->Writeln(u"Hello world!");

    auto callback = MakeObject<ExFontSettings::FontSubstitutionWarningCollector>();
    doc->set_WarningCallback(callback);

    // Store the current collection of font sources, which will be the default font source for every document
    // for which we do not specify a different font source.
    ArrayPtr<SharedPtr<FontSourceBase>> originalFontSources = FontSettings::get_DefaultInstance()->GetFontsSources();

    // For testing purposes, we will set Aspose.Words to look for fonts only in a folder that does not exist.
    FontSettings::get_DefaultInstance()->SetFontsFolder(String::Empty, false);

    // When rendering the document, there will be no place to find the "Times New Roman" font.
    // This will cause a font substitution warning, which our callback will detect.
    doc->Save(ArtifactsDir + u"FontSettings.SubstitutionWarning.pdf");

    FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);

    ASSERT_TRUE(callback->FontSubstitutionWarnings->idx_get(0)->get_WarningType() == WarningType::FontSubstitution);
    ASSERT_TRUE(System::ObjectExt::Equals(callback->FontSubstitutionWarnings->idx_get(0)->get_Description(),
                                          u"Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
}

class FontSubstitutionWarningCollector : public IWarningCallback
{
public:
    SharedPtr<WarningInfoCollection> FontSubstitutionWarnings;

    void Warning(SharedPtr<WarningInfo> info) override
    {
        if (info->get_WarningType() == WarningType::FontSubstitution)
        {
            FontSubstitutionWarnings->Warning(info);
        }
    }

    FontSubstitutionWarningCollector() : FontSubstitutionWarnings(MakeObject<WarningInfoCollection>())
    {
    }
};
```

## See Also

* Class [FontSettings](../)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
