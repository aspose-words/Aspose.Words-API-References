---
title: "Aspose::Words::Fonts::FontInfo clase"
linktitle: "FontInfo"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::FontInfo clase. Especifica información sobre una fuente utilizada en el documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.fonts/fontinfo/
---
## FontInfo class


Especifica información sobre una fuente utilizada en el documento. Para obtener más información, visite el artículo de documentación [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontInfo : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_AltName](./get_altname/)() const | Obtiene o establece el nombre alternativo de la fuente. |
| [get_Charset](./get_charset/)() | Obtiene o establece el conjunto de caracteres de la fuente. |
| [get_EmbeddingLicensingRights](./get_embeddinglicensingrights/)() | Obtiene los derechos de licencia de la fuente incrustada. |
| [get_Family](./get_family/)() const | Obtiene o establece la familia tipográfica a la que pertenece esta fuente. |
| [get_IsTrueType](./get_istruetype/)() const | Indica que esta fuente es una fuente TrueType u OpenType en contraposición a una fuente raster o vectorial. El valor predeterminado es **true**. |
| [get_Name](./get_name/)() const | Obtiene el nombre de la fuente. |
| [get_Panose](./get_panose/)() const | Obtiene o establece el número de clasificación tipográfica PANOSE. |
| [get_Pitch](./get_pitch/)() const | El pitch indica si la fuente es de ancho fijo, espaciada proporcionalmente, o depende de una configuración predeterminada. |
| [GetEmbeddedFont](./getembeddedfont/)(Aspose::Words::Fonts::EmbeddedFontFormat, Aspose::Words::Fonts::EmbeddedFontStyle) | Obtiene un archivo de fuente incrustado específico. |
| [GetEmbeddedFontAsOpenType](./getembeddedfontasopentype/)(Aspose::Words::Fonts::EmbeddedFontStyle) | Obtiene un archivo de fuente incrustado en formato OpenType. [Fonts](../) en formato Embedded OpenType se convierten a OpenType. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AltName](./set_altname/)(const System::String\&) | Establecedor para [Aspose::Words::Fonts::FontInfo::get_AltName](./get_altname/). |
| [set_Charset](./set_charset/)(int32_t) | Establecedor para [Aspose::Words::Fonts::FontInfo::get_Charset](./get_charset/). |
| [set_Family](./set_family/)(Aspose::Words::Fonts::FontFamily) | Establecedor para [Aspose::Words::Fonts::FontInfo::get_Family](./get_family/). |
| [set_IsTrueType](./set_istruetype/)(bool) | Establecedor para [Aspose::Words::Fonts::FontInfo::get_IsTrueType](./get_istruetype/). |
| [set_Panose](./set_panose/)(const System::ArrayPtr\<uint8_t\>\&) | Establecedor para [Aspose::Words::Fonts::FontInfo::get_Panose](./get_panose/). |
| [set_Pitch](./set_pitch/)(Aspose::Words::Fonts::FontPitch) | Establecedor para [Aspose::Words::Fonts::FontInfo::get_Pitch](./get_pitch/). |
| static [Type](./type/)() |  |
## Observaciones


No crea instancias de esta clase directamente. Utilice la propiedad [FontInfos](../../aspose.words/documentbase/get_fontinfos/) para acceder a la colección de fuentes definidas en un documento.

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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
