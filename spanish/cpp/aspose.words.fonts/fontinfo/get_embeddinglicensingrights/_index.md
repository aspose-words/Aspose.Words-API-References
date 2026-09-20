---
title: "Método Aspose::Words::Fonts::FontInfo::get_EmbeddingLicensingRights"
linktitle: "get_EmbeddingLicensingRights"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fonts::FontInfo::get_EmbeddingLicensingRights. Obtiene los derechos de licencia de la fuente incrustada en C++."
type: docs
weight: 3500
url: /es/cpp/aspose.words.fonts/fontinfo/get_embeddinglicensingrights/
---
## FontInfo::get_EmbeddingLicensingRights method


Obtiene los derechos de licencia de la fuente incrustada.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontEmbeddingLicensingRights> Aspose::Words::Fonts::FontInfo::get_EmbeddingLicensingRights()
```

## Observaciones


El valor puede ser **null** si la fuente no está incrustada.

## Ejemplos



Muestra cómo obtener información de derechos de licencia para fuentes incrustadas ([FontInfo](../)).
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

* Class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
