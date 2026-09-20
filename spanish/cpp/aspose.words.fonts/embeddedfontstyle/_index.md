---
title: "Aspose::Words::Fonts::EmbeddedFontStyle enum"
linktitle: "EmbeddedFontStyle"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::EmbeddedFontStyle enum. Especifica el estilo de una fuente incrustada dentro de un objeto FontInfo en C++."
type: docs
weight: 20000
url: /es/cpp/aspose.words.fonts/embeddedfontstyle/
---
## EmbeddedFontStyle enum


Especifica el estilo de una fuente incrustada dentro de un objeto [FontInfo](../fontinfo/).

```cpp
enum class EmbeddedFontStyle
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Regular | 0 | Especifica la fuente incrustada Regular. |
| Negrita | 1 | Especifica la fuente incrustada Negrita. |
| Cursiva | 2 | Especifica la fuente incrustada Cursiva. |
| NegritaCursiva | 3 | Especifica la fuente incrustada Negrita-Cursiva. |


## Ejemplos



Muestra cómo extraer una fuente incrustada de un documento y guardarla en el sistema de archivos local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfo> embeddedFont = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift");
System::ArrayPtr<uint8_t> embeddedFontBytes = embeddedFont->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.ttf", embeddedFontBytes);

// Los formatos de fuentes incrustadas pueden ser diferentes en otros formatos como .doc.
// Necesitamos conocer el formato correcto antes de poder extraer la fuente.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.doc");

ASSERT_TRUE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::OpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFont(Aspose::Words::Fonts::EmbeddedFontFormat::EmbeddedOpenType, Aspose::Words::Fonts::EmbeddedFontStyle::Regular)));

// Además, podemos convertir el formato OpenType incrustado, que proviene de documentos .doc, a OpenType.
embeddedFontBytes = doc->get_FontInfos()->idx_get(u"Alte DIN 1451 Mittelschrift")->GetEmbeddedFontAsOpenType(Aspose::Words::Fonts::EmbeddedFontStyle::Regular);

System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Alte DIN 1451 Mittelschrift.otf", embeddedFontBytes);
```

## Ver también

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
