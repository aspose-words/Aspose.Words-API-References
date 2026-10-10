---
title: "Aspose::Words::WarningSource enum"
linktitle: "WarningSource"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::WarningSource enum. Especifica el módulo que produce una advertancia durante la carga o guardado del documento en C++."
type: docs
weight: 128000
url: /es/cpp/aspose.words/warningsource/
---
## WarningSource enum


Especifica el módulo que genera una advertencia durante la carga o guardado del documento.

```cpp
enum class WarningSource
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Desconocido | 0 | No se ha especificado la fuente de la advertencia. |
| Diseño | 1 | Módulo que crea el diseño de un documento. |
| DrawingML | 2 | Módulo que renderiza formas DrawingML. |
| OfficeMath | 3 | Módulo que renderiza OfficeMath. |
| Formas | 4 | Módulo que renderiza formas ordinarias. |
| Metarchivo | 5 | Módulo que renderiza metaficheros. |
| Xps | 6 | Módulo que renderiza XPS. |
| Pdf | 7 | Módulo que renderiza PDF. |
| Image | 8 | Módulo que renderiza imágenes. |
| Docx | 9 | Módulo que lee/escribe archivos DOCX. |
| Doc | 10 | Módulo que lee/escribe archivos DOC binarios. |
| Text | 11 | Módulo que lee/escribe archivos de texto plano. |
| Rtf | 12 | Módulo que lee/escribe archivos RTF. |
| WordML | 13 | Módulo que lee/escribe archivos WML. |
| Nrx | 14 | Módulos comunes que se comparten entre los módulos lector/escritor DOCX/WML. |
| Odt | 15 | Módulo que lee/escribe archivos ODT. |
| Html | 16 | Módulo que lee/escribe archivos HTML/MHTML. |
| Validador | 17 | Módulo que verifica la consistencia y validez del modelo. |
| Xaml | 18 | Módulo que lee/escribe archivos Xaml. |
| Svm | 19 | Módulo que lee archivos Svm. |
| MathML | 20 | Módulo que lee archivos MathML de W3C. |
| Fuente | 21 | Módulo que lee archivos de fuentes. |
| Svg | 22 | Módulo que lee archivos SVG. |
| Markdown | 23 | Módulo que lee/escribe archivos Markdown. |
| Chm | 24 | Módulo que lee archivos CHM. |
| Epub | 25 | Módulo que lee/escribe archivos EPUB. |
| Xml | 26 | Módulo que lee archivos XML. |
| Xlsx | 27 | Módulo que escribe archivos XLSX. |
| Docling | 28 | Módulo que escribe archivos JSON de Docling. |


## Ejemplos



Muestra cómo trabajar con la fuente de advertencias.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Emphases markdown warning.docx");

auto warnings = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warnings);
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.EmphasesWarningSourceMarkdown.md");

for (auto&& warningInfo : warnings)
{
    if (warningInfo->get_Source() == Aspose::Words::WarningSource::Markdown)
    {
        ASSERT_EQ(u"The (*, 0:11) cannot be properly written into Markdown.", warningInfo->get_Description());
    }
}
```


Muestra cómo obtener información adicional sobre la sustitución de fuentes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto callback = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(callback);

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->SetFontsFolder(get_FontsDir(), false);
fontSettings->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Arial", System::MakeArray<System::String>({u"Arvo", u"Slab"}));

doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.SubstitutionWarnings.pdf");

auto warningInfo = System::ExplicitCast<Aspose::Words::FontSubstitutionWarningInfo>(callback->idx_get(0));
ASSERT_EQ(Aspose::Words::WarningSource::Layout, warningInfo->get_Source());
ASSERT_EQ(Aspose::Words::WarningType::FontSubstitution, warningInfo->get_WarningType());
ASSERT_EQ(Aspose::Words::FontSubstitutionReason::TableSubstitutionRule, warningInfo->get_Reason());
ASSERT_EQ(u"Font \'Arial\' has not been found. Using \'Arvo\' font instead. Reason: table substitution.", warningInfo->get_Description());
ASSERT_TRUE(warningInfo->get_RequestedBold());
ASSERT_FALSE(warningInfo->get_RequestedItalic());
ASSERT_EQ(u"Arial", warningInfo->get_RequestedFamilyName());
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
