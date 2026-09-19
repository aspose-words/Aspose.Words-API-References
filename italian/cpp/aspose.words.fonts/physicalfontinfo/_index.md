---
title: "Aspose::Words::Fonts::PhysicalFontInfo classe"
linktitle: "PhysicalFontInfo"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::PhysicalFontInfo classe. Specifica le informazioni sul carattere fisico disponibile per il motore di caratteri di Aspose.Words. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class


Specifica le informazioni sul carattere fisico disponibile per il motore dei caratteri di Aspose.Words. Per saperne di più, visita l'articolo di documentazione [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class PhysicalFontInfo : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_EmbeddingLicensingRights](./get_embeddinglicensingrights/)() const | Incorporamento dei diritti di licenza per il carattere. |
| [get_FilePath](./get_filepath/)() const | Percorso al file del carattere, se presente. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | Nome della famiglia del carattere. |
| [get_FullFontName](./get_fullfontname/)() const | Nome completo del carattere. |
| [get_Version](./get_version/)() const | Stringa di versione del carattere. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Esempi



Mostra come elencare i caratteri disponibili.
```cpp
// Configura Aspose.Words per prelevare i caratteri da una cartella personalizzata, e poi stampa ogni carattere disponibile.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> folderFontSource = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true)});

for (auto&& fontInfo : System::IterateOver(folderFontSource[0]->GetAvailableFonts()))
{
    std::cout << "FontFamilyName : " << fontInfo->get_FontFamilyName() << std::endl;
    std::cout << "FullFontName  : " << fontInfo->get_FullFontName() << std::endl;
    std::cout << "Version  : " << fontInfo->get_Version() << std::endl;
    std::cout << "FilePath : " << fontInfo->get_FilePath() << "\n" << std::endl;
}
```

## Vedi anche

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
