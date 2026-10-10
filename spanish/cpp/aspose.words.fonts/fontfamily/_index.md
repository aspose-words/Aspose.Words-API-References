---
title: "Aspose::Words::Fonts::FontFamily enumeración"
linktitle: "FontFamily"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontFamily enumeración. Representa la familia de fuentes en C++."
type: docs
weight: 21000
url: /es/cpp/aspose.words.fonts/fontfamily/
---
## FontFamily enum


Representa la familia de fuentes.

```cpp
enum class FontFamily
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Auto | 0 | Especifica un nombre de familia genérico. Este nombre se usa cuando la información sobre una fuente no existe o no importa. Se utiliza la fuente predeterminada. |
| Romano | 1 | Especifica una fuente proporcional con serifas. Un ejemplo es Times New Roman. |
| Suizo | 2 | Especifica una fuente proporcional sin serifas. Un ejemplo es Arial. |
| Moderna | 3 | Especifica una fuente monoespaciada con o sin serifas. Las fuentes monoespaciadas suelen ser modernas; ejemplos incluyen Pica, Elite y Courier New. |
| Script | 4 | Especifica una fuente diseñada para parecer escritura a mano; ejemplos incluyen Script y Cursive. |
| Decorativa | 5 | Especifica una fuente de novedad. Un ejemplo es Old English. |

## Observaciones


Una familia de fuentes es un conjunto de fuentes que comparten ancho de trazo y características de serifas.

## Ejemplos



Muestra cómo acceder e imprimir los detalles de cada fuente en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>> fontCollectionEnumerator = doc->get_FontInfos()->GetEnumerator();
while (fontCollectionEnumerator->MoveNext())
{
    System::SharedPtr<Aspose::Words::Fonts::FontInfo> fontInfo = fontCollectionEnumerator->get_Current();
    if (fontInfo != nullptr)
    {
        std::cout << (System::String(u"Font name: ") + fontInfo->get_Name()) << std::endl;

        // Los nombres alternativos suelen estar en blanco.
        std::cout << (System::String(u"Alt name: ") + fontInfo->get_AltName()) << std::endl;
        std::cout << (System::String(u"\t- Family: ") + System::ObjectExt::ToString(fontInfo->get_Family())) << std::endl;
        std::cout << (System::String(u"\t- ") + (fontInfo->get_IsTrueType() ? System::String(u"Is TrueType") : System::String(u"Is not TrueType"))) << std::endl;
        std::cout << (System::String(u"\t- Pitch: ") + System::ObjectExt::ToString(fontInfo->get_Pitch())) << std::endl;
        std::cout << (System::String(u"\t- Charset: ") + fontInfo->get_Charset()) << std::endl;
        std::cout << "\t- Panose:" << std::endl;
        std::cout << (System::String(u"\t\tFamily Kind: ") + fontInfo->get_Panose()[0]) << std::endl;
        std::cout << (System::String(u"\t\tSerif Style: ") + fontInfo->get_Panose()[1]) << std::endl;
        std::cout << (System::String(u"\t\tWeight: ") + fontInfo->get_Panose()[2]) << std::endl;
        std::cout << (System::String(u"\t\tProportion: ") + fontInfo->get_Panose()[3]) << std::endl;
        std::cout << (System::String(u"\t\tContrast: ") + fontInfo->get_Panose()[4]) << std::endl;
        std::cout << (System::String(u"\t\tStroke Variation: ") + fontInfo->get_Panose()[5]) << std::endl;
        std::cout << (System::String(u"\t\tArm Style: ") + fontInfo->get_Panose()[6]) << std::endl;
        std::cout << (System::String(u"\t\tLetterform: ") + fontInfo->get_Panose()[7]) << std::endl;
        std::cout << (System::String(u"\t\tMidline: ") + fontInfo->get_Panose()[8]) << std::endl;
        std::cout << (System::String(u"\t\tX-Height: ") + fontInfo->get_Panose()[9]) << std::endl;
    }
}
```

## Ver también

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
