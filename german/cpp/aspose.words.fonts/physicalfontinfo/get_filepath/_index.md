---
title: "Aspose::Words::Fonts::PhysicalFontInfo::get_FilePath Methode"
linktitle: "get_FilePath"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::PhysicalFontInfo::get_FilePath Methode. Pfad zur Schriftdatei, falls vorhanden, in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fonts/physicalfontinfo/get_filepath/
---
## PhysicalFontInfo::get_FilePath method


Pfad zur Schriftartdatei, falls vorhanden.

```cpp
System::String Aspose::Words::Fonts::PhysicalFontInfo::get_FilePath() const
```


## Beispiele



Zeigt, wie verfügbare Schriftarten aufgelistet werden.
```cpp
// Konfigurieren Sie Aspose.Words, um Schriftarten aus einem benutzerdefinierten Ordner zu beziehen, und geben Sie anschließend jede verfügbare Schriftart aus.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> folderFontSource = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true)});

for (auto&& fontInfo : System::IterateOver(folderFontSource[0]->GetAvailableFonts()))
{
    std::cout << "FontFamilyName : " << fontInfo->get_FontFamilyName() << std::endl;
    std::cout << "FullFontName  : " << fontInfo->get_FullFontName() << std::endl;
    std::cout << "Version  : " << fontInfo->get_Version() << std::endl;
    std::cout << "FilePath : " << fontInfo->get_FilePath() << "\n" << std::endl;
}
```

## Siehe auch

* Class [PhysicalFontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
