---
title: "Aspose::Words::Fonts::FontInfo::get_Name metodo"
linktitle: "get_Name"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontInfo::get_Name method. Ottiene il nome del font in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.fonts/fontinfo/get_name/
---
## FontInfo::get_Name method


Ottiene il nome del carattere.

```cpp
System::String Aspose::Words::Fonts::FontInfo::get_Name() const
```

## Note


Non può essere **null**. Può essere una stringa vuota.

## Esempi



Mostra come stampare i dettagli dei caratteri presenti in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Stampa tutti i caratteri utilizzati e non utilizzati nel documento.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```

## Vedi anche

* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
