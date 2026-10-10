---
title: "Metodo Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_NoSubsetting"
linktitle: "get_NoSubsetting"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_NoSubsetting. Indica la restrizione \"No subsetting\" in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.fonts/fontembeddinglicensingrights/get_nosubsetting/
---
## FontEmbeddingLicensingRights::get_NoSubsetting method


Indica la restrizione "No subsetting".

```cpp
bool Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_NoSubsetting() const
```


## Esempi



Mostra come ottenere le informazioni sui diritti di licenza per i font incorporati ([FontInfo](../../fontinfo/)).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font rights.docx");

// Ottieni l'elenco dei font del documento.
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

## Vedi anche

* Class [FontEmbeddingLicensingRights](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
