---
title: "Aspose::Words::Fonts::FontFamily énum"
linktitle: "FontFamily"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontFamily énum. Représente la famille de polices en C++."
type: docs
weight: 21000
url: /fr/cpp/aspose.words.fonts/fontfamily/
---
## FontFamily enum


Représente la famille de police.

```cpp
enum class FontFamily
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Auto | 0 | Spécifie un nom de famille générique. Ce nom est utilisé lorsque les informations sur une police n'existent pas ou n'ont pas d'importance. La police par défaut est utilisée. |
| Roman | 1 | Spécifie une police proportionnelle avec empattements. Un exemple est Times New Roman. |
| Swiss | 2 | Spécifie une police proportionnelle sans empattements. Un exemple est Arial. |
| Modern | 3 | Spécifie une police à chasse fixe avec ou sans empattements. Les polices à chasse fixe sont généralement modernes ; des exemples incluent Pica, Elite et Courier New. |
| Script | 4 | Spécifie une police conçue pour ressembler à une écriture manuscrite ; des exemples incluent Script et Cursive. |
| Decorative | 5 | Spécifie une police fantaisie. Un exemple est Old English. |

## Remarques


Une famille de polices est un ensemble de polices ayant une largeur de traits et des caractéristiques d'empattement communes.

## Exemples



Montre comment accéder et imprimer les détails de chaque police dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>> fontCollectionEnumerator = doc->get_FontInfos()->GetEnumerator();
while (fontCollectionEnumerator->MoveNext())
{
    System::SharedPtr<Aspose::Words::Fonts::FontInfo> fontInfo = fontCollectionEnumerator->get_Current();
    if (fontInfo != nullptr)
    {
        std::cout << (System::String(u"Font name: ") + fontInfo->get_Name()) << std::endl;

        // Les noms alternatifs sont généralement vides.
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

## Voir aussi

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
