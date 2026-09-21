---
title: "Aspose::Words::Fonts::FontEmbeddingUsagePermissions enum"
linktitle: "FontEmbeddingUsagePermissions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontEmbeddingUsagePermissions enum. Representerar teckensnittsinbäddningsanvändningsbehörigheterna i C++."
type: docs
weight: 20500
url: /sv/cpp/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enum


Representerar behörigheterna för användning av teckensnittsinbäddning.

```cpp
enum class FontEmbeddingUsagePermissions
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Installable | 0 | Teckensnittet kan bäddas in och kan installeras permanent för användning på fjärrsystem, eller för användning av andra användare. |
| RestrictedLicense | 1 | Teckensnittet får inte modifieras, bäddas in eller bytas ut på något sätt utan att först erhålla uttryckligt tillstånd från den rättsliga ägaren. |
| PrintAndPreview | 2 | Teckensnittet kan bäddas in och kan tillfälligt laddas på andra system för att visa eller skriva ut dokumentet. |
| Editable | 3 | Teckensnittet kan bäddas in och kan tillfälligt laddas på andra system. |


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
