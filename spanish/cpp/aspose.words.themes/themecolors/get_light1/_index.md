---
title: "Aspose::Words::Themes::ThemeColors::get_Light1 método"
linktitle: "get_Light1"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Themes::ThemeColors::get_Light1 método. Especifica el color Light 1 en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.themes/themecolors/get_light1/
---
## ThemeColors::get_Light1 method


Especifica el color Light 1.

```cpp
System::Drawing::Color Aspose::Words::Themes::ThemeColors::get_Light1()
```


## Ejemplos



Muestra cómo establecer colores y fuentes personalizados para los temas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Theme colors.docx");

// El objeto "Theme" nos brinda acceso al tema del documento, una fuente de fuentes y colores predeterminados.
System::SharedPtr<Aspose::Words::Themes::Theme> theme = doc->get_Theme();

// Algunos estilos, como "Heading 1" y "Subtitle", heredarán estas fuentes.
theme->get_MajorFonts()->set_Latin(u"Courier New");
theme->get_MinorFonts()->set_Latin(u"Agency FB");

// Otros idiomas también pueden tener sus fuentes personalizadas en este tema.
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_EastAsian());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_EastAsian());

// La propiedad "Colors" contiene la paleta de colores de Microsoft Word,
// que aparece al cambiar el sombreado o el color de fuente.
// Aplica colores personalizados a la paleta de colores para que tengamos fácil acceso a ellos en Microsoft Word
// cuando, por ejemplo, cambiamos el color de fuente a través de "Home" -> "Font" -> "Font Color",
// o insertamos una forma y luego establecemos un color para ella a través de "Shape Format" -> "Shape Styles".
System::SharedPtr<Aspose::Words::Themes::ThemeColors> colors = theme->get_Colors();
colors->set_Dark1(System::Drawing::Color::get_MidnightBlue());
colors->set_Light1(System::Drawing::Color::get_PaleGreen());
colors->set_Dark2(System::Drawing::Color::get_Indigo());
colors->set_Light2(System::Drawing::Color::get_Khaki());

colors->set_Accent1(System::Drawing::Color::get_OrangeRed());
colors->set_Accent2(System::Drawing::Color::get_LightSalmon());
colors->set_Accent3(System::Drawing::Color::get_Yellow());
colors->set_Accent4(System::Drawing::Color::get_Gold());
colors->set_Accent5(System::Drawing::Color::get_BlueViolet());
colors->set_Accent6(System::Drawing::Color::get_DarkViolet());

// Aplica colores personalizados a los hipervínculos en sus estados pulsado y sin pulsar.
colors->set_Hyperlink(System::Drawing::Color::get_Black());
colors->set_FollowedHyperlink(System::Drawing::Color::get_Gray());

doc->Save(get_ArtifactsDir() + u"Themes.CustomColorsAndFonts.docx");
```

## Ver también

* Class [ThemeColors](../)
* Namespace [Aspose::Words::Themes](../../)
* Library [Aspose.Words for C++](../../../)
