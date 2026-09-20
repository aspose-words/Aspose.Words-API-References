---
title: "Aspose::Words::Themes::ThemeColors class"
linktitle: "ThemeColors"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Themes::ThemeColors class. Representa el esquema de colores del tema del documento, que contiene doce colores. El objeto ThemeColors contiene seis colores de acento, dos colores oscuros, dos colores claros y un color para cada hipervínculo y para el hipervínculo visitado en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.themes/themecolors/
---
## ThemeColors class


Representa el esquema de colores del tema del documento, que contiene doce colores. El objeto [ThemeColors](./) contiene seis colores de acento, dos colores oscuros, dos colores claros y un color para cada hipervínculo y para el hipervínculo visitado.

```cpp
class ThemeColors : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Accent1](./get_accent1/)() | Especifica el color Accent 1. |
| [get_Accent2](./get_accent2/)() | Especifica el color Accent 2. |
| [get_Accent3](./get_accent3/)() | Especifica el color Accent 3. |
| [get_Accent4](./get_accent4/)() | Especifica el color Accent 4. |
| [get_Accent5](./get_accent5/)() | Especifica el color Accent 5. |
| [get_Accent6](./get_accent6/)() | Especifica el color Accent 6. |
| [get_Dark1](./get_dark1/)() | Especifica el color Dark 1. |
| [get_Dark2](./get_dark2/)() | Especifica el color Dark 2. |
| [get_FollowedHyperlink](./get_followedhyperlink/)() | Especifica el color para un hipervínculo visitado. |
| [get_Hyperlink](./get_hyperlink/)() | Especifica el color para un hipervínculo. |
| [get_Light1](./get_light1/)() | Especifica el color Light 1. |
| [get_Light2](./get_light2/)() | Especifica el color Light 2. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Accent1](./set_accent1/)(System::Drawing::Color) | Método setter para [Aspose::Words::Themes::ThemeColors::get_Accent1](./get_accent1/). |
| [set_Accent2](./set_accent2/)(System::Drawing::Color) | Método setter para [Aspose::Words::Themes::ThemeColors::get_Accent2](./get_accent2/). |
| [set_Accent3](./set_accent3/)(System::Drawing::Color) | Método setter para [Aspose::Words::Themes::ThemeColors::get_Accent3](./get_accent3/). |
| [set_Accent4](./set_accent4/)(System::Drawing::Color) | Establecedor de [Aspose::Words::Themes::ThemeColors::get_Accent4](./get_accent4/). |
| [set_Accent5](./set_accent5/)(System::Drawing::Color) | Establecedor de [Aspose::Words::Themes::ThemeColors::get_Accent5](./get_accent5/). |
| [set_Accent6](./set_accent6/)(System::Drawing::Color) | Establecedor de [Aspose::Words::Themes::ThemeColors::get_Accent6](./get_accent6/). |
| [set_Dark1](./set_dark1/)(System::Drawing::Color) | Establecedor de [Aspose::Words::Themes::ThemeColors::get_Dark1](./get_dark1/). |
| [set_Dark2](./set_dark2/)(System::Drawing::Color) | Establecedor de [Aspose::Words::Themes::ThemeColors::get_Dark2](./get_dark2/). |
| [set_FollowedHyperlink](./set_followedhyperlink/)(System::Drawing::Color) | Establecedor de [Aspose::Words::Themes::ThemeColors::get_FollowedHyperlink](./get_followedhyperlink/). |
| [set_Hyperlink](./set_hyperlink/)(System::Drawing::Color) | Establecedor de [Aspose::Words::Themes::ThemeColors::get_Hyperlink](./get_hyperlink/). |
| [set_Light1](./set_light1/)(System::Drawing::Color) | Establecedor de [Aspose::Words::Themes::ThemeColors::get_Light1](./get_light1/). |
| [set_Light2](./set_light2/)(System::Drawing::Color) | Establecedor de [Aspose::Words::Themes::ThemeColors::get_Light2](./get_light2/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Themes](../)
* Library [Aspose.Words for C++](../../)
