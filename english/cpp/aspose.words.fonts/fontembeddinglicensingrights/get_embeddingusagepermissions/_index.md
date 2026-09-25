---
title: Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_EmbeddingUsagePermissions method
linktitle: get_EmbeddingUsagePermissions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_EmbeddingUsagePermissions method. Usage permissions in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.fonts/fontembeddinglicensingrights/get_embeddingusagepermissions/
---
## FontEmbeddingLicensingRights::get_EmbeddingUsagePermissions method


Usage permissions.

```cpp
Aspose::Words::Fonts::FontEmbeddingUsagePermissions Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_EmbeddingUsagePermissions() const
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

* Enum [FontEmbeddingUsagePermissions](../../fontembeddingusagepermissions/)
* Class [FontEmbeddingLicensingRights](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
