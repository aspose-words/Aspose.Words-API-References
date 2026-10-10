---
title: "Aspose::Words::Fonts::FontEmbeddingUsagePermissions enum"
linktitle: "FontEmbeddingUsagePermissions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontEmbeddingUsagePermissions enum. Représente les autorisations d’utilisation de l’incorporation de police en C++."
type: docs
weight: 20500
url: /fr/cpp/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enum


Représente les autorisations d'utilisation de l'incorporation de police.

```cpp
enum class FontEmbeddingUsagePermissions
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Installable | 0 | La police peut être incorporée et peut être installée de façon permanente pour être utilisée sur des systèmes distants, ou pour être utilisée par d’autres utilisateurs. |
| RestrictedLicense | 1 | La police ne doit pas être modifiée, incorporée ou échangée de quelque manière que ce soit sans obtenir d’abord l’autorisation explicite du propriétaire légal. |
| PrintAndPreview | 2 | La police peut être incorporée et peut être chargée temporairement sur d’autres systèmes aux fins de visualisation ou d’impression du document. |
| Editable | 3 | La police peut être incorporée et peut être chargée temporairement sur d’autres systèmes. |


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
