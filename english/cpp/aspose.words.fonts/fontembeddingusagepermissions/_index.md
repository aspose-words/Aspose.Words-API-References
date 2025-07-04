---
title: Aspose::Words::Fonts::FontEmbeddingUsagePermissions enum
linktitle: FontEmbeddingUsagePermissions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontEmbeddingUsagePermissions enum. Represents the font embedding usage permissions in C++.'
type: docs
weight: 20500
url: /cpp/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enum


Represents the font embedding usage permissions.

```cpp
enum class FontEmbeddingUsagePermissions
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Installable | 0 | The font may be embedded, and may be permanently installed for use on a remote systems, or for use by other users. |
| RestrictedLicense | 1 | The font must not be modified, embedded or exchanged in any manner without first obtaining explicit permission of the legal owner. |
| PrintAndPreview | 2 | The font may be embedded, and may be temporarily loaded on other systems for purposes of viewing or printing the document. |
| Editable | 3 | The font may be embedded, and may be temporarily loaded on other systems. |


## Examples



Shows how to get license rights information for embedded fonts ([FontInfo](../fontinfo/)). 
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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
