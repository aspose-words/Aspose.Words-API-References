---
title: "Aspose::Words::FontSubstitutionWarningInfo::get_RequestedFamilyName método"
linktitle: "get_RequestedFamilyName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::FontSubstitutionWarningInfo::get_RequestedFamilyName método. Nombre de familia de fuente solicitado en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/fontsubstitutionwarninginfo/get_requestedfamilyname/
---
## FontSubstitutionWarningInfo::get_RequestedFamilyName method


Nombre de familia de fuente solicitado.

```cpp
System::String Aspose::Words::FontSubstitutionWarningInfo::get_RequestedFamilyName() const
```


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

* Class [FontSubstitutionWarningInfo](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
