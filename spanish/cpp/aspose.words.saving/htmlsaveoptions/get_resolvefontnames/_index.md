---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames método"
linktitle: "get_ResolveFontNames"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames método. Especifica si los nombres de familia de fuentes usados en el documento se resuelven y sustituyen según FontSettings al escribirse en formatos basados en HTML en C++."
type: docs
weight: 42000
url: /es/cpp/aspose.words.saving/htmlsaveoptions/get_resolvefontnames/
---
## HtmlSaveOptions::get_ResolveFontNames method


Especifica si los nombres de familia de fuentes usados en el documento se resuelven y sustituyen según [FontSettings](../../../aspose.words/document/get_fontsettings/) al escribirse en formatos basados en HTML.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames() const
```

## Observaciones


Por defecto, esta opción está establecida en **false** y los nombres de familia de fuentes se escriben en HTML tal como aparecen en los documentos de origen. Es decir, [FontSettings](../../../aspose.words/document/get_fontsettings/) se ignoran y no se realiza ninguna resolución o sustitución de los nombres de familia de fuentes.

Si esta opción se establece en **true**, Aspose.Words usa [FontSettings](../../../aspose.words/document/get_fontsettings/) para resolver cada nombre de familia de fuentes especificado en un documento de origen al nombre de una familia de fuentes disponible, realizando la sustitución de fuentes según sea necesario.

## Ejemplos



Muestra cómo resolver todos los nombres de fuentes antes de escribirlos en HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Este documento contiene texto que menciona una fuente que no tenemos.
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"28 Days Later")));

// Si no tenemos forma de obtener esta fuente, y queremos poder mostrar todo el texto
// en este documento en un HTML de salida, podemos sustituirla por otra fuente.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_Enabled(true);

doc->set_FontSettings(fontSettings);

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
// Por defecto, esta opción está establecida en 'False' y Aspose.Words escribe los nombres de fuente tal como se especifican en el documento original.
saveOptions->set_ResolveFontNames(resolveFontNames);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html");

ASSERT_TRUE(resolveFontNames ? System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:Arial\">")->get_Success() : System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:\'28 Days Later\'\">")->get_Success());
```

## Ver también

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
