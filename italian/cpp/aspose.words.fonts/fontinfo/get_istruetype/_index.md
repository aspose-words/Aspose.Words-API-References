---
title: "Aspose::Words::Fonts::FontInfo::get_IsTrueType metodo"
linktitle: "get_IsTrueType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontInfo::get_IsTrueType metodo. Indica che questo carattere è un font TrueType o OpenType, a differenza di un font raster o vettoriale. Il valore predefinito è true in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.fonts/fontinfo/get_istruetype/
---
## FontInfo::get_IsTrueType method


Indica che questo font è un font TrueType o OpenType, a differenza di un font raster o vettoriale. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::Fonts::FontInfo::get_IsTrueType() const
```


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
