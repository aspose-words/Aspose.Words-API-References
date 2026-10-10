---
title: "Aspose::Words::Fonts::FontEmbeddingUsagePermissions enum"
linktitle: "FontEmbeddingUsagePermissions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontEmbeddingUsagePermissions enum. Rappresenta le autorizzazioni di utilizzo dell'incorporamento dei font in C++."
type: docs
weight: 20500
url: /it/cpp/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enum


Rappresenta le autorizzazioni di utilizzo per l'incorporamento dei caratteri.

```cpp
enum class FontEmbeddingUsagePermissions
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Installabile | 0 | Il font può essere incorporato e può essere installato permanentemente per l'uso su sistemi remoti, o per l'uso da parte di altri utenti. |
| RestrictedLicense | 1 | Il font non deve essere modificato, incorporato o scambiato in alcun modo senza prima ottenere l'esplicita autorizzazione del proprietario legale. |
| PrintAndPreview | 2 | Il font può essere incorporato e può essere caricato temporaneamente su altri sistemi per scopi di visualizzazione o stampa del documento. |
| Modificabile | 3 | Il font può essere incorporato e può essere caricato temporaneamente su altri sistemi. |


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
