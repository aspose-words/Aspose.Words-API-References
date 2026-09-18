---
title: "Aspose::Words::Fonts::PhysicalFontInfo Klasse"
linktitle: "PhysicalFontInfo"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::PhysicalFontInfo Klasse. Gibt Informationen über physische Schriftarten an, die der Aspose.Words‑Schrift-Engine zur Verfügung stehen. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 15000
url: /de/cpp/aspose.words.fonts/physicalfontinfo/
---
## PhysicalFontInfo class


Gibt Informationen über physische Schriftarten an, die der Aspose.Words-Schrift-Engine zur Verfügung stehen. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class PhysicalFontInfo : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_EmbeddingLicensingRights](./get_embeddinglicensingrights/)() const | Einbettungs‑Lizenzrechte für die Schriftart. |
| [get_FilePath](./get_filepath/)() const | Pfad zur Schriftartdatei, falls vorhanden. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | Familienname der Schriftart. |
| [get_FullFontName](./get_fullfontname/)() const | Vollständiger Name der Schriftart. |
| [get_Version](./get_version/)() const | Versionszeichenfolge der Schriftart. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
