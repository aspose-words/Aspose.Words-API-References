---
title: "Aspose::Words::Fonts::FontEmbeddingLicensingRights klass"
linktitle: "FontEmbeddingLicensingRights"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontEmbeddingLicensingRights klass. Representerar inbäddningslicensrättigheter för teckensnittet i C++."
type: docs
weight: 4500
url: /sv/cpp/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class


Representerar inbäddningslicensrättigheter för teckensnittet.

```cpp
class FontEmbeddingLicensingRights : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_BitmapEmbeddingOnly](./get_bitmapembeddingonly/)() const | Indikerar restriktionen "Endast bitmapinbäddning". |
| [get_EmbeddingUsagePermissions](./get_embeddingusagepermissions/)() const | Användarbehörigheter. |
| [get_NoSubsetting](./get_nosubsetting/)() const | Indikerar restriktionen "Ingen delmängd". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Exempel



Visar hur man får licensrättsinformation för inbäddade teckensnitt ([FontInfo](../fontinfo/)).
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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
