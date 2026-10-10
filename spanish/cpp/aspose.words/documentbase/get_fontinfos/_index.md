---
title: "Aspose::Words::DocumentBase::get_FontInfos método"
linktitle: "get_FontInfos"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBase::get_FontInfos método. Proporciona acceso a las propiedades de las fuentes usadas en este documento en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/documentbase/get_fontinfos/
---
## DocumentBase::get_FontInfos method


Proporciona acceso a las propiedades de las fuentes utilizadas en este documento.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> Aspose::Words::DocumentBase::get_FontInfos() const
```

## Observaciones


Esta colección de definiciones de fuentes se carga tal cual desde el documento. Las definiciones de [Font](../../font/) pueden ser opcionales, faltar o estar incompletas en algunos documentos.

No confíe en esta colección para determinar que una fuente en particular se usa en el documento. Sólo debe usar esta colección para obtener información sobre fuentes que podrían usarse en el documento.

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


Muestra cómo guardar un documento con fuentes TrueType incrustadas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```

## Ver también

* Class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
