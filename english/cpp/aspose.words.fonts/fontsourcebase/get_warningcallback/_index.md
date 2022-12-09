---
title: get_WarningCallback
second_title: Aspose.Words for C++ API Reference
description: Called during processing of font source when an issue is detected that might result in formatting fidelity loss.
type: docs
weight: 40
url: /cpp/aspose.words.fonts/fontsourcebase/get_warningcallback/
---
## FontSourceBase::get_WarningCallback method


Called during processing of font source when an issue is detected that might result in formatting fidelity loss.

```cpp
System::SharedPtr<Aspose::Words::IWarningCallback> Aspose::Words::Fonts::FontSourceBase::get_WarningCallback() const
```


## Examples



Shows how to call warning callback when the font sources working with. 
```cpp
void FontSourceWarning()
{
    auto settings = MakeObject<FontSettings>();
    settings->SetFontsFolder(u"bad folder?", false);

    SharedPtr<FontSourceBase> source = settings->GetFontsSources()->idx_get(0);
    auto callback = MakeObject<ExFontSettings::FontSourceWarningCollector>();
    source->set_WarningCallback(callback);

    // Get the list of fonts to call warning callback.
    SharedPtr<System::Collections::Generic::IList<SharedPtr<PhysicalFontInfo>>> fontInfos = source->GetAvailableFonts();

    ASSERT_TRUE(callback->FontSubstitutionWarnings->idx_get(0)->get_Description().Contains(u"Error loading font from the folder \"bad folder?\""));
}

class FontSourceWarningCollector : public IWarningCallback
{
public:
    SharedPtr<WarningInfoCollection> FontSubstitutionWarnings;

    void Warning(SharedPtr<WarningInfo> info) override
    {
        FontSubstitutionWarnings->Warning(info);
    }

    FontSourceWarningCollector() : FontSubstitutionWarnings(MakeObject<WarningInfoCollection>())
    {
    }
};
```

## See Also

* Interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words](../../../)
