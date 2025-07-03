---
title: Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly method
linktitle: get_BitmapEmbeddingOnly
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly method. Indicates the "Bitmap embedding only" restriction in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.fonts/fontembeddinglicensingrights/get_bitmapembeddingonly/
---
## FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly method


Indicates the "Bitmap embedding only" restriction.

```cpp
bool Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly() const
```


## Examples



Shows how to get license rights information for embedded fonts ([FontInfo](../../fontinfo/)). 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font rights.docx");

// Get the list of document fonts.
System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
for (auto&& fontInfo : fontInfos)
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

* Class [FontEmbeddingLicensingRights](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
