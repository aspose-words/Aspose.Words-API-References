---
title: "Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_NoSubsetting méthode"
linktitle: "get_NoSubsetting"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_NoSubsetting méthode. Indique la restriction \"No subsetting\" en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.fonts/fontembeddinglicensingrights/get_nosubsetting/
---
## FontEmbeddingLicensingRights::get_NoSubsetting method


Indique la restriction « Pas de sous-ensemble ».

```cpp
bool Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_NoSubsetting() const
```


## Exemples



Montre comment obtenir les informations de droits de licence pour les polices incorporées ([FontInfo](../../fontinfo/)).
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

* Class [FontEmbeddingLicensingRights](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
