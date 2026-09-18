---
title: "Aspose::Words::Fonts::FontInfo::get_Name-Methode"
linktitle: "get_Name"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontInfo::get_Name-Methode. Ruft den Namen der Schrift in C++ ab."
type: docs
weight: 6000
url: /de/cpp/aspose.words.fonts/fontinfo/get_name/
---
## FontInfo::get_Name method


Liest den Namen der Schrift.

```cpp
System::String Aspose::Words::Fonts::FontInfo::get_Name() const
```

## Hinweise


Darf nicht **null** sein. Kann eine leere Zeichenkette sein.

## Beispiele



Zeigt, wie man die Details der im Dokument vorhandenen Schriften ausgibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Gibt alle verwendeten und nicht verwendeten Schriften im Dokument aus.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```

## Siehe auch

* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
