---
title: "Aspose::Words::Fonts::FontInfo::get_Name método"
linktitle: "get_Name"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fonts::FontInfo::get_Name. Obtiene el nombre de la fuente en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.fonts/fontinfo/get_name/
---
## FontInfo::get_Name method


Obtiene el nombre de la fuente.

```cpp
System::String Aspose::Words::Fonts::FontInfo::get_Name() const
```

## Observaciones


No puede ser **null**. Puede ser una cadena vacía.

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
