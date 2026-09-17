---
title: "Aspose::Words::Themes::ThemeColors classe"
linktitle: "ThemeColors"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Themes::ThemeColors classe. Représente le schéma de couleurs du thème du document qui contient douze couleurs. L'objet ThemeColors contient six couleurs d'accent, deux couleurs sombres, deux couleurs claires et une couleur pour chaque hyperlien et hyperlien visité en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.themes/themecolors/
---
## ThemeColors class


Représente le schéma de couleurs du thème du document qui contient douze couleurs. L'objet [ThemeColors](./) contient six couleurs d'accent, deux couleurs sombres, deux couleurs claires et une couleur pour chaque hyperlien et hyperlien visité.

```cpp
class ThemeColors : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Accent1](./get_accent1/)() | Spécifie la couleur Accent 1. |
| [get_Accent2](./get_accent2/)() | Spécifie la couleur Accent 2. |
| [get_Accent3](./get_accent3/)() | Spécifie la couleur Accent 3. |
| [get_Accent4](./get_accent4/)() | Spécifie la couleur Accent 4. |
| [get_Accent5](./get_accent5/)() | Spécifie la couleur Accent 5. |
| [get_Accent6](./get_accent6/)() | Spécifie la couleur Accent 6. |
| [get_Dark1](./get_dark1/)() | Spécifie la couleur Dark 1. |
| [get_Dark2](./get_dark2/)() | Spécifie la couleur Dark 2. |
| [get_FollowedHyperlink](./get_followedhyperlink/)() | Spécifie la couleur d'un hyperlien cliqué. |
| [get_Hyperlink](./get_hyperlink/)() | Spécifie la couleur d'un hyperlien. |
| [get_Light1](./get_light1/)() | Spécifie la couleur Light 1. |
| [get_Light2](./get_light2/)() | Spécifie la couleur Light 2. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Accent1](./set_accent1/)(System::Drawing::Color) | Mutateur pour [Aspose::Words::Themes::ThemeColors::get_Accent1](./get_accent1/). |
| [set_Accent2](./set_accent2/)(System::Drawing::Color) | Mutateur pour [Aspose::Words::Themes::ThemeColors::get_Accent2](./get_accent2/). |
| [set_Accent3](./set_accent3/)(System::Drawing::Color) | Mutateur pour [Aspose::Words::Themes::ThemeColors::get_Accent3](./get_accent3/). |
| [set_Accent4](./set_accent4/)(System::Drawing::Color) | Définisseur de [Aspose::Words::Themes::ThemeColors::get_Accent4](./get_accent4/). |
| [set_Accent5](./set_accent5/)(System::Drawing::Color) | Définisseur de [Aspose::Words::Themes::ThemeColors::get_Accent5](./get_accent5/). |
| [set_Accent6](./set_accent6/)(System::Drawing::Color) | Définisseur de [Aspose::Words::Themes::ThemeColors::get_Accent6](./get_accent6/). |
| [set_Dark1](./set_dark1/)(System::Drawing::Color) | Définisseur de [Aspose::Words::Themes::ThemeColors::get_Dark1](./get_dark1/). |
| [set_Dark2](./set_dark2/)(System::Drawing::Color) | Définisseur de [Aspose::Words::Themes::ThemeColors::get_Dark2](./get_dark2/). |
| [set_FollowedHyperlink](./set_followedhyperlink/)(System::Drawing::Color) | Définisseur de [Aspose::Words::Themes::ThemeColors::get_FollowedHyperlink](./get_followedhyperlink/). |
| [set_Hyperlink](./set_hyperlink/)(System::Drawing::Color) | Définisseur de [Aspose::Words::Themes::ThemeColors::get_Hyperlink](./get_hyperlink/). |
| [set_Light1](./set_light1/)(System::Drawing::Color) | Définisseur de [Aspose::Words::Themes::ThemeColors::get_Light1](./get_light1/). |
| [set_Light2](./set_light2/)(System::Drawing::Color) | Définisseur de [Aspose::Words::Themes::ThemeColors::get_Light2](./get_light2/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment définir des couleurs et des polices personnalisées pour les thèmes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Theme colors.docx");

// L'objet "Theme" nous donne accès au thème du document, une source de polices et de couleurs par défaut.
System::SharedPtr<Aspose::Words::Themes::Theme> theme = doc->get_Theme();

// Certaines styles, comme "Heading 1" et "Subtitle", hériteront de ces polices.
theme->get_MajorFonts()->set_Latin(u"Courier New");
theme->get_MinorFonts()->set_Latin(u"Agency FB");

// D'autres langues peuvent également avoir leurs polices personnalisées dans ce thème.
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_EastAsian());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_EastAsian());

// La propriété "Colors" contient la palette de couleurs de Microsoft Word,
// qui apparaît lors du changement d’ombrage ou de couleur de police.
// Appliquez des couleurs personnalisées à la palette de couleurs afin de les rendre facilement accessibles dans Microsoft Word
// lorsque nous, par exemple, changeons la couleur de police via "Home" -> "Font" -> "Font Color",
// ou insérons une forme, puis définissons une couleur pour celle-ci via "Shape Format" -> "Shape Styles".
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

// Appliquez des couleurs personnalisées aux hyperliens dans leurs états cliqué et non cliqué.
colors->set_Hyperlink(System::Drawing::Color::get_Black());
colors->set_FollowedHyperlink(System::Drawing::Color::get_Gray());

doc->Save(get_ArtifactsDir() + u"Themes.CustomColorsAndFonts.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Themes](../)
* Library [Aspose.Words for C++](../../)
