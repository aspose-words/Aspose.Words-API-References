---
title: "Aspose::Words::Fonts::FontInfo::get_IsTrueType método"
linktitle: "get_IsTrueType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontInfo::get_IsTrueType método. Indica que esta fuente es una fuente TrueType u OpenType en contraposición a una fuente raster o vectorial. El valor predeterminado es true en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.fonts/fontinfo/get_istruetype/
---
## FontInfo::get_IsTrueType method


Indica que esta fuente es una fuente TrueType u OpenType en contraposición a una fuente raster o vectorial. El valor predeterminado es **true**.

```cpp
bool Aspose::Words::Fonts::FontInfo::get_IsTrueType() const
```


## Ejemplos



Muestra cómo imprimir los detalles de qué fuentes están presentes en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Imprima todas las fuentes usadas y no usadas en el documento.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```

## Ver también

* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
