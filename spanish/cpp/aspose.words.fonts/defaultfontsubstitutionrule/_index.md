---
title: "Clase Aspose::Words::Fonts::DefaultFontSubstitutionRule"
linktitle: "DefaultFontSubstitutionRule"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Fonts::DefaultFontSubstitutionRule. Regla de sustitución de fuentes predeterminada. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class


Regla predeterminada de sustitución de fuentes. Para obtener más información, visite el artículo de documentación [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class DefaultFontSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_DefaultFontName](./get_defaultfontname/)() | Obtiene o establece el nombre de la fuente predeterminada. |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Especifica si la regla está habilitada o no. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DefaultFontName](./set_defaultfontname/)(const System::String\&) | Establecedor para [Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName](./get_defaultfontname/). |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Establecedor para [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| static [Type](./type/)() |  |

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

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
