---
title: "Aspose::Words::Fonts::FontFamily enum"
linktitle: "FontFamily"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontFamily enum. Rappresenta la famiglia di caratteri in C++."
type: docs
weight: 21000
url: /it/cpp/aspose.words.fonts/fontfamily/
---
## FontFamily enum


Rappresenta la famiglia di caratteri.

```cpp
enum class FontFamily
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Auto | 0 | Specifica un nome di famiglia generico. Questo nome è usato quando le informazioni su un carattere non esistono o non sono rilevanti. Viene usato il carattere predefinito. |
| Roman | 1 | Specifica un carattere proporzionale con grazie. Un esempio è Times New Roman. |
| Swiss | 2 | Specifica un carattere proporzionale senza grazie. Un esempio è Arial. |
| Modern | 3 | Specifica un carattere monospazio con o senza grazie. I caratteri monospazio sono solitamente moderni; esempi includono Pica, Elite e Courier New. |
| Script | 4 | Specifica un carattere progettato per assomigliare alla scrittura a mano; esempi includono Script e Cursive. |
| Decorative | 5 | Specifica un carattere di novità. Un esempio è Old English. |

## Note


Una famiglia di caratteri è un insieme di caratteri che hanno la stessa larghezza di tratto e caratteristiche di grazie.

## Esempi



Mostra come accedere e stampare i dettagli di ciascun carattere in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>> fontCollectionEnumerator = doc->get_FontInfos()->GetEnumerator();
while (fontCollectionEnumerator->MoveNext())
{
    System::SharedPtr<Aspose::Words::Fonts::FontInfo> fontInfo = fontCollectionEnumerator->get_Current();
    if (fontInfo != nullptr)
    {
        std::cout << (System::String(u"Font name: ") + fontInfo->get_Name()) << std::endl;

        // I nomi alternativi sono solitamente vuoti.
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

## Vedi anche

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
