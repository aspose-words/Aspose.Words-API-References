---
title: "Aspose::Words::Fonts::FontInfo::get_EmbeddingLicensingRights metodo"
linktitle: "get_EmbeddingLicensingRights"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontInfo::get_EmbeddingLicensingRights metodo. Ottiene i diritti di licenza del font incorporato in C++."
type: docs
weight: 3500
url: /it/cpp/aspose.words.fonts/fontinfo/get_embeddinglicensingrights/
---
## FontInfo::get_EmbeddingLicensingRights method


Ottiene i diritti di licenza del font incorporato.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontEmbeddingLicensingRights> Aspose::Words::Fonts::FontInfo::get_EmbeddingLicensingRights()
```

## Note


Il valore può essere null se il font non è incorporato.

## Esempi



Mostra come ottenere le informazioni sui diritti di licenza per i font incorporati ([FontInfo](../)).
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

* Class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
