---
title: "Aspose::Words::Fonts::FontFamily Aufzählung"
linktitle: "FontFamily"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontFamily Aufzählung. Stellt die Schriftfamilie in C++ dar."
type: docs
weight: 21000
url: /de/cpp/aspose.words.fonts/fontfamily/
---
## FontFamily enum


Stellt die Schriftfamilie dar.

```cpp
enum class FontFamily
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Auto | 0 | Gibt einen generischen Familiennamen an. Dieser Name wird verwendet, wenn Informationen über eine Schriftart nicht vorhanden oder irrelevant sind. Die Standardschriftart wird verwendet. |
| Roman | 1 | Gibt eine proportionale Schriftart mit Serifen an. Ein Beispiel ist Times New Roman. |
| Swiss | 2 | Gibt eine proportionale Schrift ohne Serifen an. Ein Beispiel ist Arial. |
| Modern | 3 | Gibt eine Monospace-Schrift mit oder ohne Serifen an. Monospace-Schriften sind normalerweise modern; Beispiele sind Pica, Elite und Courier New. |
| Script | 4 | Gibt eine Schrift an, die wie Handschrift gestaltet ist; Beispiele sind Script und Cursive. |
| Dekorativ | 5 | Gibt eine Sonderfont an. Ein Beispiel ist Old English. |

## Hinweise


Eine Schriftfamilie ist eine Gruppe von Schriften mit gemeinsamer Strichstärke und Serifeneigenschaften.

## Beispiele



Zeigt, wie man auf die Details jeder Schrift in einem Dokument zugreift und sie ausgibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>> fontCollectionEnumerator = doc->get_FontInfos()->GetEnumerator();
while (fontCollectionEnumerator->MoveNext())
{
    System::SharedPtr<Aspose::Words::Fonts::FontInfo> fontInfo = fontCollectionEnumerator->get_Current();
    if (fontInfo != nullptr)
    {
        std::cout << (System::String(u"Font name: ") + fontInfo->get_Name()) << std::endl;

        // Alternativnamen sind normalerweise leer.
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

## Siehe auch

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
