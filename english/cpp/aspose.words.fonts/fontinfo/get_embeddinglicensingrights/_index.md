---
title: Aspose::Words::Fonts::FontInfo::get_EmbeddingLicensingRights method
linktitle: get_EmbeddingLicensingRights
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontInfo::get_EmbeddingLicensingRights method. Gets the embedded font licensing rights in C++.'
type: docs
weight: 3500
url: /cpp/aspose.words.fonts/fontinfo/get_embeddinglicensingrights/
---
## FontInfo::get_EmbeddingLicensingRights method


Gets the embedded font licensing rights.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontEmbeddingLicensingRights> Aspose::Words::Fonts::FontInfo::get_EmbeddingLicensingRights()
```

## Remarks


The value may be null if font is not embedded.

## Examples



Shows how to get license rights information for embedded fonts ([FontInfo](../)). 
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

* Class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
