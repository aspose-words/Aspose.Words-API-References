---
title: "Aspose::Words::Fonts::PhysicalFontInfo::get_Version metodo"
linktitle: "get_Version"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::PhysicalFontInfo::get_Version metodo. Stringa della versione del carattere in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.fonts/physicalfontinfo/get_version/
---
## PhysicalFontInfo::get_Version method


Stringa di versione del carattere.

```cpp
System::String Aspose::Words::Fonts::PhysicalFontInfo::get_Version() const
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

* Class [PhysicalFontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
