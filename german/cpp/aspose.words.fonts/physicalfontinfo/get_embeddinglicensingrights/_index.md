---
title: "Aspose::Words::Fonts::PhysicalFontInfo::get_EmbeddingLicensingRights Methode"
linktitle: "get_EmbeddingLicensingRights"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::PhysicalFontInfo::get_EmbeddingLicensingRights Methode. Einbettungs-Lizenzrechte für die Schrift in C++."
type: docs
weight: 1500
url: /de/cpp/aspose.words.fonts/physicalfontinfo/get_embeddinglicensingrights/
---
## PhysicalFontInfo::get_EmbeddingLicensingRights method


Einbettungs‑Lizenzrechte für die Schriftart.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::FontEmbeddingLicensingRights> & Aspose::Words::Fonts::PhysicalFontInfo::get_EmbeddingLicensingRights() const
```


## Beispiele



Zeigt, wie man Lizenzrechtsinformationen für eingebettete Schriften erhält ([PhysicalFontInfo](../)).
```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> settings = Aspose::Words::Fonts::FontSettings::get_DefaultInstance();
System::SharedPtr<Aspose::Words::Fonts::FontSourceBase> source = settings->GetFontsSources()->idx_get(0);

// Rufen Sie die Liste der verfügbaren Schriften ab.
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

## Siehe auch

* Class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* Class [PhysicalFontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
