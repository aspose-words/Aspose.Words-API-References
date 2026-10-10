---
title: "Aspose::Words::Fonts::FontInfo::get_EmbeddingLicensingRights metod"
linktitle: "get_EmbeddingLicensingRights"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontInfo::get_EmbeddingLicensingRights method. Hämtar de inbäddade teckensnittens licensrättigheter i C++."
type: docs
weight: 3500
url: /sv/cpp/aspose.words.fonts/fontinfo/get_embeddinglicensingrights/
---
## FontInfo::get_EmbeddingLicensingRights method


Hämtar de inbäddade teckensnittens licensrättigheter.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontEmbeddingLicensingRights> Aspose::Words::Fonts::FontInfo::get_EmbeddingLicensingRights()
```

## Anmärkningar


Värdet kan vara null om teckensnittet inte är inbäddat.

## Exempel



Visar hur man får licensrättighetsinformation för inbäddade teckensnitt ([FontInfo](../)).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font rights.docx");

// Hämta listan över dokumentets teckensnitt.
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

## Se även

* Class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
