---
title: "Aspose::Words::Fonts::FontSourceBase::GetAvailableFonts-Methode"
linktitle: "GetAvailableFonts"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontSourceBase::GetAvailableFonts-Methode. Gibt eine Liste der über diese Quelle verfügbaren Schriftarten in C++ zurück."
type: docs
weight: 5000
url: /de/cpp/aspose.words.fonts/fontsourcebase/getavailablefonts/
---
## FontSourceBase::GetAvailableFonts method


Gibt eine Liste der über diese Quelle verfügbaren Schriften zurück.

```cpp
System::SharedPtr<System::Collections::Generic::IList<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>>> Aspose::Words::Fonts::FontSourceBase::GetAvailableFonts()
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

* Class [PhysicalFontInfo](../../physicalfontinfo/)
* Class [FontSourceBase](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
