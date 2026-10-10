---
title: "Aspose::Words::Fonts::FontEmbeddingLicensingRights class"
linktitle: "FontEmbeddingLicensingRights"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontEmbeddingLicensingRights class. Représente les droits de licence d'intégration pour la police en C++."
type: docs
weight: 4500
url: /fr/cpp/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class


Représente les droits d’intégration de licence pour la police.

```cpp
class FontEmbeddingLicensingRights : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_BitmapEmbeddingOnly](./get_bitmapembeddingonly/)() const | Indique la restriction « Intégration bitmap uniquement ». |
| [get_EmbeddingUsagePermissions](./get_embeddingusagepermissions/)() const | Permissions d'utilisation. |
| [get_NoSubsetting](./get_nosubsetting/)() const | Indique la restriction « Pas de sous-ensemble ». |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Exemples



Montre comment obtenir les informations de droits de licence pour les polices incorporées ([FontInfo](../fontinfo/)).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font rights.docx");

// Obtenez la liste des polices du document.
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

## Voir aussi

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
