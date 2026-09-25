---
title: Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_NoSubsetting method
linktitle: get_NoSubsetting
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_NoSubsetting method. Indicates the "No subsetting" restriction in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.fonts/fontembeddinglicensingrights/get_nosubsetting/
---
## FontEmbeddingLicensingRights::get_NoSubsetting method


Indicates the "No subsetting" restriction.

```cpp
bool Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_NoSubsetting() const
```


## Examples



Shows how to get license rights information for embedded fonts ([FontInfo](../../fontinfo/)). 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Embedded font rights.docx"));

// Get the list of document fonts.
System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
for (auto&& fontInfo : fontInfos)
{
    if (fontInfo->get_EmbeddingLicensingRights() != nullptr)
    {
        System::Console::WriteLine(System::ExplicitCast<System::Object>(fontInfo->get_EmbeddingLicensingRights()->get_EmbeddingUsagePermissions()));
        System::Console::WriteLine(fontInfo->get_EmbeddingLicensingRights()->get_BitmapEmbeddingOnly());
        System::Console::WriteLine(fontInfo->get_EmbeddingLicensingRights()->get_NoSubsetting());
    }
}
```

## See Also

* Class [FontEmbeddingLicensingRights](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
