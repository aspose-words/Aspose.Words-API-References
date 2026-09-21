---
title: "Aspose::Words::Fonts::FontFamily enum"
linktitle: "FontFamily"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontFamily enum. Representerar teckensnittsfamiljen i C++."
type: docs
weight: 21000
url: /sv/cpp/aspose.words.fonts/fontfamily/
---
## FontFamily enum


Representerar teckensnittsfamiljen.

```cpp
enum class FontFamily
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Auto | 0 | Anger ett generiskt familjenamn. Detta namn används när information om ett teckensnitt inte finns eller är irrelevant. Standardteckensnittet används. |
| Roman | 1 | Anger ett proportionellt teckensnitt med seriffer. Ett exempel är Times New Roman. |
| Swiss | 2 | Anger ett proportionellt teckensnitt utan seriffer. Ett exempel är Arial. |
| Modern | 3 | Anger ett monospace‑teckensnitt med eller utan seriffer. Monospace‑teckensnitt är vanligtvis moderna; exempel inkluderar Pica, Elite och Courier New. |
| Script | 4 | Anger ett teckensnitt som är utformat för att likna handskrift; exempel inkluderar Script och Cursive. |
| Dekorativ | 5 | Anger ett novelty‑teckensnitt. Ett exempel är Old English. |

## Anmärkningar


En teckensnittsfamilj är en uppsättning teckensnitt med gemensam streckbredd och seriffegenskaper.

## Exempel



Visar hur man får åtkomst till och skriver ut detaljer för varje teckensnitt i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>> fontCollectionEnumerator = doc->get_FontInfos()->GetEnumerator();
while (fontCollectionEnumerator->MoveNext())
{
    System::SharedPtr<Aspose::Words::Fonts::FontInfo> fontInfo = fontCollectionEnumerator->get_Current();
    if (fontInfo != nullptr)
    {
        std::cout << (System::String(u"Font name: ") + fontInfo->get_Name()) << std::endl;

        // Alternativa namn är vanligtvis tomma.
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

## Se även

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
