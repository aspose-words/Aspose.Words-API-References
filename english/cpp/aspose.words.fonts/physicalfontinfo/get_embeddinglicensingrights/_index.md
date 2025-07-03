---
title: Aspose::Words::Fonts::PhysicalFontInfo::get_EmbeddingLicensingRights method
linktitle: get_EmbeddingLicensingRights
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::PhysicalFontInfo::get_EmbeddingLicensingRights method. Embedding licensing rights for the font in C++.'
type: docs
weight: 1500
url: /cpp/aspose.words.fonts/physicalfontinfo/get_embeddinglicensingrights/
---
## PhysicalFontInfo::get_EmbeddingLicensingRights method


Embedding licensing rights for the font.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::FontEmbeddingLicensingRights> & Aspose::Words::Fonts::PhysicalFontInfo::get_EmbeddingLicensingRights() const
```


## Examples



Shows how to get license rights information for embedded fonts ([PhysicalFontInfo](../)). 
```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> settings = Aspose::Words::Fonts::FontSettings::get_DefaultInstance();
System::SharedPtr<Aspose::Words::Fonts::FontSourceBase> source = settings->GetFontsSources()->idx_get(0);

// Get the list of available fonts.
System::SharedPtr<System::Collections::Generic::IList<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>>> fontInfos = source->GetAvailableFonts();
for (auto&& fontInfo : System::IterateOver(fontInfos))
{
    if (fontInfo->get_EmbeddingLicensingRights() != nullptr)
    {
        std::cout << System::EnumGetName(fontInfo->get_EmbeddingLicensingRights()->get_EmbeddingUsagePermissions()) << std::endl;
        std::cout << System::Convert::ToString(fontInfo->get_EmbeddingLicensingRights()->get_BitmapEmbeddingOnly()) << std::endl;
        std::cout << System::Convert::ToString(fontInfo->get_EmbeddingLicensingRights()->get_NoSubsetting()) << std::endl;
    }
}
```

## See Also

* Class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* Class [PhysicalFontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
