---
title: "Método Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution"
linktitle: "get_DefaultFontSubstitution"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution. Configuraciones relacionadas con la regla de sustitución de fuente predeterminada en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fonts/fontsubstitutionsettings/get_defaultfontsubstitution/
---
## FontSubstitutionSettings::get_DefaultFontSubstitution method


[Settings](../../../aspose.words.settings/) related to default font substitution rule.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> & Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution() const
```


## Ejemplos



Muestra cómo establecer la regla de sustitución de fuentes predeterminada.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Obtenga la regla de sustitución predeterminada dentro de FontSettings.
// Esta regla sustituirá todas las fuentes faltantes por "Times New Roman".
System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> defaultFontSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution();
ASSERT_TRUE(defaultFontSubstitutionRule->get_Enabled());
ASSERT_EQ(u"Times New Roman", defaultFontSubstitutionRule->get_DefaultFontName());

// Establezca el sustituto de fuente predeterminado a "Courier New".
defaultFontSubstitutionRule->set_DefaultFontName(u"Courier New");

// Usando un constructor de documentos, agregue texto en una fuente que no tenemos para ver que se produzca la sustitución,
// y luego renderice el resultado en un PDF.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Missing Font");
builder->Writeln(u"Line written in a missing font, which will be substituted with Courier New.");

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontSubstitutionRule.pdf");
```

## Ver también

* Class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* Class [FontSubstitutionSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
