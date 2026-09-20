---
title: "Aspose::Words::Fonts::FontInfo::GetEmbeddedFontAsOpenType método"
linktitle: "GetEmbeddedFontAsOpenType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontInfo::GetEmbeddedFontAsOpenType método. Obtiene un archivo de fuente incrustado en formato OpenType. Las fuentes en formato Embedded OpenType se convierten a OpenType en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.fonts/fontinfo/getembeddedfontasopentype/
---
## FontInfo::GetEmbeddedFontAsOpenType method


Obtiene un archivo de fuente incrustado en formato OpenType. [Fonts](../../) en formato Embedded OpenType se convierten a OpenType.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Fonts::FontInfo::GetEmbeddedFontAsOpenType(Aspose::Words::Fonts::EmbeddedFontStyle style)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| estilo | Aspose::Words::Fonts::EmbeddedFontStyle | Especifica el estilo de fuente a recuperar. |

### ReturnValue

Devuelve **null** si la fuente especificada no está incrustada.

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

* Enum [EmbeddedFontStyle](../../embeddedfontstyle/)
* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
