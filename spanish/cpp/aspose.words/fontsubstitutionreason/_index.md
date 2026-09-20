---
title: "Aspose::Words::FontSubstitutionReason enumeración"
linktitle: "FontSubstitutionReason"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::FontSubstitutionReason enumeración. Especifica la razón de la sustitución de fuentes en C++."
type: docs
weight: 89500
url: /es/cpp/aspose.words/fontsubstitutionreason/
---
## FontSubstitutionReason enum


Especifica la razón de la sustitución de fuentes.

```cpp
enum class FontSubstitutionReason
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| AlternativeName | 0 | [Font](../font/) sustitución por nombre alternativo del documento. |
| FontNameSubstitutionRule | 1 | [Font](../font/) sustitución por regla de nombre de fuente. |
| FontConfigSubstitutionRule | 2 | [Font](../font/) sustitución por regla de configuración de fuente. |
| TableSubstitutionRule | 3 | [Font](../font/) sustitución por regla de tabla. |
| FontInfoSubstitutionRule | 4 | [Font](../font/) sustitución por regla de información de fuente. |
| DefaultFontSubstitutionRule | 5 | [Font](../font/) sustitución por regla de fuente predeterminada. |
| FirstAvailableFont | 6 | [Font](../font/) sustitución con la primera fuente disponible. |


## Ejemplos



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
