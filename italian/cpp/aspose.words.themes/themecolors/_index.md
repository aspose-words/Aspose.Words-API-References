---
title: "Aspose::Words::Themes::ThemeColors class"
linktitle: "ThemeColors"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Themes::ThemeColors class. Rappresenta lo schema di colori del tema del documento, che contiene dodici colori. L'oggetto ThemeColors contiene sei colori di accento, due colori scuri, due colori chiari e un colore per ciascun collegamento ipertestuale e per il collegamento ipertestuale visitato in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.themes/themecolors/
---
## ThemeColors class


Rappresenta lo schema di colori del tema del documento, che contiene dodici colori. L'oggetto [ThemeColors](./) contiene sei colori di accento, due colori scuri, due colori chiari e un colore per ciascun collegamento ipertestuale e per il collegamento ipertestuale visitato.

```cpp
class ThemeColors : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Accent1](./get_accent1/)() | Specifica il colore Accento 1. |
| [get_Accent2](./get_accent2/)() | Specifica il colore Accento 2. |
| [get_Accent3](./get_accent3/)() | Specifica il colore Accento 3. |
| [get_Accent4](./get_accent4/)() | Specifica il colore Accento 4. |
| [get_Accent5](./get_accent5/)() | Specifica il colore Accento 5. |
| [get_Accent6](./get_accent6/)() | Specifica il colore Accento 6. |
| [get_Dark1](./get_dark1/)() | Specifica il colore Scuro 1. |
| [get_Dark2](./get_dark2/)() | Specifica il colore Scuro 2. |
| [get_FollowedHyperlink](./get_followedhyperlink/)() | Specifica il colore per un collegamento ipertestuale cliccato. |
| [get_Hyperlink](./get_hyperlink/)() | Specifica il colore per un collegamento ipertestuale. |
| [get_Light1](./get_light1/)() | Specifica il colore Chiaro 1. |
| [get_Light2](./get_light2/)() | Specifica il colore Chiaro 2. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Accent1](./set_accent1/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Themes::ThemeColors::get_Accent1](./get_accent1/). |
| [set_Accent2](./set_accent2/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Themes::ThemeColors::get_Accent2](./get_accent2/). |
| [set_Accent3](./set_accent3/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Themes::ThemeColors::get_Accent3](./get_accent3/). |
| [set_Accent4](./set_accent4/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Themes::ThemeColors::get_Accent4](./get_accent4/). |
| [set_Accent5](./set_accent5/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Themes::ThemeColors::get_Accent5](./get_accent5/). |
| [set_Accent6](./set_accent6/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Themes::ThemeColors::get_Accent6](./get_accent6/). |
| [set_Dark1](./set_dark1/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Themes::ThemeColors::get_Dark1](./get_dark1/). |
| [set_Dark2](./set_dark2/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Themes::ThemeColors::get_Dark2](./get_dark2/). |
| [set_FollowedHyperlink](./set_followedhyperlink/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Themes::ThemeColors::get_FollowedHyperlink](./get_followedhyperlink/). |
| [set_Hyperlink](./set_hyperlink/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Themes::ThemeColors::get_Hyperlink](./get_hyperlink/). |
| [set_Light1](./set_light1/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Themes::ThemeColors::get_Light1](./get_light1/). |
| [set_Light2](./set_light2/)(System::Drawing::Color) | Impostatore per [Aspose::Words::Themes::ThemeColors::get_Light2](./get_light2/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come impostare colori e caratteri personalizzati per i temi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Theme colors.docx");

// L'oggetto "Theme" ci dà accesso al tema del documento, una fonte di caratteri e colori predefiniti.
System::SharedPtr<Aspose::Words::Themes::Theme> theme = doc->get_Theme();

// Alcuni stili, come "Heading 1" e "Subtitle", erediteranno questi caratteri.
theme->get_MajorFonts()->set_Latin(u"Courier New");
theme->get_MinorFonts()->set_Latin(u"Agency FB");

// Altre lingue possono anche avere i loro caratteri personalizzati in questo tema.
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_EastAsian());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_EastAsian());

// La proprietà "Colors" contiene la tavolozza dei colori di Microsoft Word,
// che appare quando si modifica l'ombreggiatura o il colore del carattere.
// Applica colori personalizzati alla tavolozza dei colori così da avervi un facile accesso in Microsoft Word
// quando, ad esempio, cambiamo il colore del carattere tramite "Home" -> "Font" -> "Font Color",
// oppure inseriamo una forma e poi impostiamo un colore per essa tramite "Shape Format" -> "Shape Styles".
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

// Applica colori personalizzati ai collegamenti ipertestuali nei loro stati cliccato e non cliccato.
colors->set_Hyperlink(System::Drawing::Color::get_Black());
colors->set_FollowedHyperlink(System::Drawing::Color::get_Gray());

doc->Save(get_ArtifactsDir() + u"Themes.CustomColorsAndFonts.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Themes](../)
* Library [Aspose.Words for C++](../../)
