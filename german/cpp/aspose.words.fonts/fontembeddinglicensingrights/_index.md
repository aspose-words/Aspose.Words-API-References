---
title: "Aspose::Words::Fonts::FontEmbeddingLicensingRights Klasse"
linktitle: "FontEmbeddingLicensingRights"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontEmbeddingLicensingRights Klasse. Stellt Einbettungs-Lizenzrechte für die Schriftart in C++ dar."
type: docs
weight: 4500
url: /de/cpp/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class


Stellt die Einbettungs‑Lizenzrechte für die Schriftart dar.

```cpp
class FontEmbeddingLicensingRights : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_BitmapEmbeddingOnly](./get_bitmapembeddingonly/)() const | Zeigt die "Bitmap embedding only" Einschränkung an. |
| [get_EmbeddingUsagePermissions](./get_embeddingusagepermissions/)() const | Nutzungsberechtigungen. |
| [get_NoSubsetting](./get_nosubsetting/)() const | Zeigt die "No subsetting" Einschränkung an. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man Lizenzrechtsinformationen für eingebettete Schriftarten erhält ([FontInfo](../fontinfo/)).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font rights.docx");

// Ruft die Liste der Dokumentenschriftarten ab.
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

## Siehe auch

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
