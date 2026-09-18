---
title: "Aspose::Words::Fonts::FontEmbeddingUsagePermissions enum"
linktitle: "FontEmbeddingUsagePermissions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontEmbeddingUsagePermissions enum. Stellt die Berechtigungen für die Schriftart‑Einbettung in C++ dar."
type: docs
weight: 20500
url: /de/cpp/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enum


Stellt die Nutzungsrechte für das Einbetten von Schriftarten dar.

```cpp
enum class FontEmbeddingUsagePermissions
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Installable | 0 | Die Schriftart kann eingebettet werden und dauerhaft installiert werden, um sie auf entfernten Systemen oder von anderen Benutzern zu verwenden. |
| RestrictedLicense | 1 | Die Schriftart darf nicht verändert, eingebettet oder in irgendeiner Weise ausgetauscht werden, ohne zuvor die ausdrückliche Erlaubnis des rechtlichen Eigentümers einzuholen. |
| PrintAndPreview | 2 | Die Schriftart kann eingebettet werden und vorübergehend auf anderen Systemen geladen werden, um das Dokument anzuzeigen oder zu drucken. |
| Editable | 3 | Die Schriftart kann eingebettet werden und vorübergehend auf anderen Systemen geladen werden. |


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
