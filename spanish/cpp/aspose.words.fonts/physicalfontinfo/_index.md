---
title: "Aspose::Words::Fonts::PhysicalFontInfo clase"
linktitle: "PhysicalFontInfo"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::PhysicalFontInfo clase. Especifica información sobre la fuente física disponible para el motor de fuentes de Aspose.Words. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class


Especifica información sobre la fuente física disponible para el motor de fuentes de Aspose.Words. Para obtener más información, visite el artículo de documentación [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class PhysicalFontInfo : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_EmbeddingLicensingRights](./get_embeddinglicensingrights/)() const | Incorporando derechos de licencia para la fuente. |
| [get_FilePath](./get_filepath/)() const | Ruta al archivo de fuente, si existe. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | Nombre de familia de la fuente. |
| [get_FullFontName](./get_fullfontname/)() const | Nombre completo de la fuente. |
| [get_Version](./get_version/)() const | Cadena de versión de la fuente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo enumerar las fuentes disponibles.
```cpp
// Configure Aspose.Words para obtener fuentes de una carpeta personalizada y luego imprima cada fuente disponible.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> folderFontSource = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true)});

for (auto&& fontInfo : System::IterateOver(folderFontSource[0]->GetAvailableFonts()))
{
    std::cout << "FontFamilyName : " << fontInfo->get_FontFamilyName() << std::endl;
    std::cout << "FullFontName  : " << fontInfo->get_FullFontName() << std::endl;
    std::cout << "Version  : " << fontInfo->get_Version() << std::endl;
    std::cout << "FilePath : " << fontInfo->get_FilePath() << "\n" << std::endl;
}
```

## Ver también

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
