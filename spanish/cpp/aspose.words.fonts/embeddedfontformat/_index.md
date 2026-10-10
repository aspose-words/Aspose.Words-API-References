---
title: "Aspose::Words::Fonts::EmbeddedFontFormat enumeración"
linktitle: "EmbeddedFontFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::EmbeddedFontFormat enum. Especifica el formato de una fuente incrustada concreta dentro del objeto FontInfo. Al guardar un documento en un archivo, solo se escriben las fuentes incrustadas del formato correspondiente en C++."
type: docs
weight: 19000
url: /es/cpp/aspose.words.fonts/embeddedfontformat/
---
## EmbeddedFontFormat enum


Especifica el formato de una fuente incrustada concreta dentro del objeto [FontInfo](../fontinfo/). Al guardar un documento en un archivo, solo se escriben las fuentes incrustadas del formato correspondiente.

```cpp
enum class EmbeddedFontFormat
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| EmbeddedOpenType | 0 | Especifica el formato de archivo Embedded OpenType (EOT). Este formato de fuentes incrustadas se utiliza en archivos DOC. |
| OpenType | 1 | Especifica la fuente, incrustada como una copia simple del archivo de fuente OpenType (TrueType). Este formato de fuentes incrustadas se utiliza en el formato Open Office XML, incluidos los archivos DOCX. |


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
