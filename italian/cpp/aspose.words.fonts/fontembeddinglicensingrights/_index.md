---
title: "Aspose::Words::Fonts::FontEmbeddingLicensingRights classe"
linktitle: "FontEmbeddingLicensingRights"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontEmbeddingLicensingRights classe. Rappresenta i diritti di licenza di incorporamento per il carattere in C++."
type: docs
weight: 4500
url: /it/cpp/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class


Rappresenta i diritti di licenza di incorporamento per il carattere.

```cpp
class FontEmbeddingLicensingRights : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_BitmapEmbeddingOnly](./get_bitmapembeddingonly/)() const | Indica la restrizione "Bitmap embedding only". |
| [get_EmbeddingUsagePermissions](./get_embeddingusagepermissions/)() const | Permessi di utilizzo. |
| [get_NoSubsetting](./get_nosubsetting/)() const | Indica la restrizione "No subsetting". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Esempi



Mostra come ottenere le informazioni sui diritti di licenza per i font incorporati ([FontInfo](../fontinfo/)).
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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
