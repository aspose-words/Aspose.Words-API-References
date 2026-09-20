---
title: "Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly método"
linktitle: "get_BitmapEmbeddingOnly"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly método. Indica la restricción \"Bitmap embedding only\" en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fonts/fontembeddinglicensingrights/get_bitmapembeddingonly/
---
## FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly method


Indica la restricción "Solo incrustación de mapa de bits".

```cpp
bool Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly() const
```


## Ejemplos



Muestra cómo obtener información de derechos de licencia para fuentes incrustadas ([FontInfo](../../fontinfo/)).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font rights.docx");

// Obtenga la lista de fuentes del documento.
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

## Ver también

* Class [FontEmbeddingLicensingRights](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
