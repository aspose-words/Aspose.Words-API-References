---
title: "Aspose::Words::Fonts::PhysicalFontInfo::get_FontFamilyName Methode"
linktitle: "get_FontFamilyName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::PhysicalFontInfo::get_FontFamilyName Methode. Familienname der Schrift in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fonts/physicalfontinfo/get_fontfamilyname/
---
## PhysicalFontInfo::get_FontFamilyName method


Familienname der Schriftart.

```cpp
System::String Aspose::Words::Fonts::PhysicalFontInfo::get_FontFamilyName() const
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
