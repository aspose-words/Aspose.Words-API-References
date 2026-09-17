---
title: "Aspose::Words::Fonts::FontInfo::get_Panose méthode"
linktitle: "get_Panose"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontInfo::get_Panose méthode. Obtient ou définit le numéro de classification de type de caractère PANOSE en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.fonts/fontinfo/get_panose/
---
## FontInfo::get_Panose method


Obtient ou définit le numéro de classification de police PANOSE.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Fonts::FontInfo::get_Panose() const
```

## Remarques


PANOSE est une description compacte de 10 octets des caractéristiques visuelles essentielles d'une police, telles que le contraste, le poids et le style sérif. Les chiffres représentent le type de famille, le [Style](../../../aspose.words/style/) sérif, le poids, la proportion, le contraste, la variation du trait, le [Style](../../../aspose.words/style/) du bras, la forme des lettres, la ligne médiane et la hauteur x.

Peut être **null**.

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

* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
