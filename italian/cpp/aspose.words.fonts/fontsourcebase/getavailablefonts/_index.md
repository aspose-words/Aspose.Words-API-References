---
title: "Metodo Aspose::Words::Fonts::FontSourceBase::GetAvailableFonts"
linktitle: "GetAvailableFonts"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fonts::FontSourceBase::GetAvailableFonts. Restituisce l'elenco dei caratteri disponibili tramite questa sorgente in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.fonts/fontsourcebase/getavailablefonts/
---
## FontSourceBase::GetAvailableFonts method


Restituisce l'elenco dei font disponibili tramite questa sorgente.

```cpp
System::SharedPtr<System::Collections::Generic::IList<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>>> Aspose::Words::Fonts::FontSourceBase::GetAvailableFonts()
```


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

* Class [PhysicalFontInfo](../../physicalfontinfo/)
* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
