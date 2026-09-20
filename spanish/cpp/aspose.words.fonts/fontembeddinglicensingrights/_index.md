---
title: "Aspose::Words::Fonts::FontEmbeddingLicensingRights clase"
linktitle: "FontEmbeddingLicensingRights"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontEmbeddingLicensingRights clase. Representa los derechos de licencia de incrustación para la fuente en C++."
type: docs
weight: 4500
url: /es/cpp/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class


Representa los derechos de licencia de incrustación para la fuente.

```cpp
class FontEmbeddingLicensingRights : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_BitmapEmbeddingOnly](./get_bitmapembeddingonly/)() const | Indica la restricción "Solo incrustación de mapa de bits". |
| [get_EmbeddingUsagePermissions](./get_embeddingusagepermissions/)() const | Permisos de uso. |
| [get_NoSubsetting](./get_nosubsetting/)() const | Indica la restricción "Sin subconjunto". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo obtener información de derechos de licencia para fuentes incrustadas ([FontInfo](../fontinfo/)).
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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
