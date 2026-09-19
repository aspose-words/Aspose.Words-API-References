---
title: "Aspose::Words::Themes::ThemeFonts class"
linktitle: "ThemeFonts"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Themes::ThemeFonts class. Rappresenta una raccolta di caratteri nello schema dei caratteri, consentendo di specificare caratteri diversi per lingue diverse: Latin, EastAsian e ComplexScript. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.themes/themefonts/
---
## ThemeFonts class


Rappresenta una raccolta di caratteri nello schema dei caratteri, consentendo di specificare caratteri diversi per lingue diverse [Latin](./get_latin/), [EastAsian](./get_eastasian/) e [ComplexScript](./get_complexscript/). Per saperne di più, visita l'articolo di documentazione [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class ThemeFonts : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_ComplexScript](./get_complexscript/)() | Specifica il nome del carattere per i caratteri ComplexScript. |
| [get_EastAsian](./get_eastasian/)() | Specifica il nome del carattere per i caratteri EastAsian. |
| [get_Latin](./get_latin/)() | Specifica il nome del carattere per i caratteri Latin. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ComplexScript](./set_complexscript/)(const System::String\&) | Impostatore per [Aspose::Words::Themes::ThemeFonts::get_ComplexScript](./get_complexscript/). |
| [set_EastAsian](./set_eastasian/)(const System::String\&) | Impostatore per [Aspose::Words::Themes::ThemeFonts::get_EastAsian](./get_eastasian/). |
| [set_Latin](./set_latin/)(const System::String\&) | Impostatore per [Aspose::Words::Themes::ThemeFonts::get_Latin](./get_latin/). |
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
