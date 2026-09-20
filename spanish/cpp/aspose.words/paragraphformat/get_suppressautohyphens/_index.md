---
title: "Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens método"
linktitle: "get_SuppressAutoHyphens"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens método. Especifica si el párrafo actual debe estar exento de cualquier hyphenation que se aplique en la configuración del documento en C++."
type: docs
weight: 38000
url: /es/cpp/aspose.words/paragraphformat/get_suppressautohyphens/
---
## ParagraphFormat::get_SuppressAutoHyphens method


Especifica si el párrafo actual debe estar exento de cualquier guionización que se aplique en la configuración del documento.

```cpp
bool Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens()
```


## Ejemplos



Muestra cómo suprimir la hyphenation para un párrafo.
```cpp
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// Abra un documento que contenga texto con una configuración regional que coincida con la de nuestro diccionario.
// Al guardar este documento en un formato de guardado de página fija, su texto tendrá hyphenation.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

// Podemos establecer la propiedad "SuppressAutoHyphens" a "true" para desactivar la hyphenation
// para un párrafo específico mientras se mantiene habilitada para el resto del documento.
// El valor predeterminado para esta propiedad es "false",
// lo que significa que, por defecto, cada párrafo usa hyphenation si está disponible.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->set_SuppressAutoHyphens(suppressAutoHyphens);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.SuppressHyphens.pdf");
```

## Ver también

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
