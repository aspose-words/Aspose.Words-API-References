---
title: "Aspose::Words::Fonts::FontEmbeddingUsagePermissions enum"
linktitle: "FontEmbeddingUsagePermissions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontEmbeddingUsagePermissions enum. Representa los permisos de uso de incrustación de fuentes en C++."
type: docs
weight: 20500
url: /es/cpp/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enum


Representa los permisos de uso de incrustación de fuentes.

```cpp
enum class FontEmbeddingUsagePermissions
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Installable | 0 | La fuente puede incrustarse y puede instalarse permanentemente para su uso en sistemas remotos, o para su uso por otros usuarios. |
| RestrictedLicense | 1 | La fuente no debe modificarse, incrustarse ni intercambiarse de ninguna manera sin obtener primero el permiso explícito del propietario legal. |
| PrintAndPreview | 2 | La fuente puede incrustarse y puede cargarse temporalmente en otros sistemas con el fin de visualizar o imprimir el documento. |
| Editable | 3 | La fuente puede incrustarse y puede cargarse temporalmente en otros sistemas. |


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
