---
title: "Aspose::Words::Themes::ThemeColor enum"
linktitle: "ThemeColor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Themes::ThemeColor enum. Spécifie les couleurs du thème pour les thèmes de document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.themes/themecolor/
---
## ThemeColor enum


Spécifie les couleurs du thème pour les thèmes de documents. Pour en savoir plus, consultez l'article de documentation [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
enum class ThemeColor
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| None | -1 | Pas de couleur. |
| Dark1 | 0 | Couleur principale sombre 1. |
| Light1 | 1 | Couleur principale claire 1. |
| Dark2 | 2 | Couleur principale sombre 2. |
| Light2 | 3 | Couleur principale claire 2. |
| Accent1 | 4 | Couleur d'accent 1. |
| Accent2 | 5 | Couleur d'accent 2. |
| Accent3 | 6 | Couleur d'accent 3. |
| Accent4 | 7 | Couleur d'accent 4. |
| Accent5 | 8 | Couleur d'accent 5. |
| Accent6 | 9 | Couleur d'accent 6. |
| Hyperlink | 10 | Couleur du lien hypertexte. |
| FollowedHyperlink | 11 | Couleur du lien hypertexte visité. |
| Text1 | 12 | Couleur du texte 1. |
| Text2 | 13 | Couleur du texte 2. |
| Background1 | 14 | Couleur d'arrière-plan 1. |
| Background2 | 15 | Couleur d'arrière-plan 2. |


## Exemples



Montre comment travailler avec les polices de thème et les couleurs.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Définissez les polices pour les langues utilisées par défaut.
doc->get_Theme()->get_MinorFonts()->set_Latin(u"Algerian");
doc->get_Theme()->get_MinorFonts()->set_EastAsian(u"Aharoni");
doc->get_Theme()->get_MinorFonts()->set_ComplexScript(u"Andalus");

System::SharedPtr<Aspose::Words::Font> font = doc->get_Styles()->idx_get(u"Normal")->get_Font();
std::cout << System::String::Format(u"Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font->get_ThemeColor(), font->get_Color()) << std::endl;

// Nous pouvons utiliser la police et la couleur de thème à la place des valeurs par défaut.
font->set_ThemeFont(Aspose::Words::Themes::ThemeFont::Minor);
font->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent2);

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::Minor, font->get_ThemeFont());
ASSERT_EQ(u"Algerian", font->get_Name());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::Minor, font->get_ThemeFontAscii());
ASSERT_EQ(u"Algerian", font->get_NameAscii());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::Minor, font->get_ThemeFontBi());
ASSERT_EQ(u"Andalus", font->get_NameBi());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::Minor, font->get_ThemeFontFarEast());
ASSERT_EQ(u"Aharoni", font->get_NameFarEast());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::Minor, font->get_ThemeFontOther());
ASSERT_EQ(u"Algerian", font->get_NameOther());

ASSERT_EQ(Aspose::Words::Themes::ThemeColor::Accent2, font->get_ThemeColor());
ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, font->get_Color());

// Il existe plusieurs façons de réinitialiser leurs polices et couleurs.
// 1 -  En définissant ThemeFont.None/ThemeColor.None:
font->set_ThemeFont(Aspose::Words::Themes::ThemeFont::None);
font->set_ThemeColor(Aspose::Words::Themes::ThemeColor::None);

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFont());
ASSERT_EQ(u"Algerian", font->get_Name());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontAscii());
ASSERT_EQ(u"Algerian", font->get_NameAscii());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontBi());
ASSERT_EQ(u"Andalus", font->get_NameBi());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontFarEast());
ASSERT_EQ(u"Aharoni", font->get_NameFarEast());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontOther());
ASSERT_EQ(u"Algerian", font->get_NameOther());

ASSERT_EQ(Aspose::Words::Themes::ThemeColor::None, font->get_ThemeColor());
ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, font->get_Color());

// 2 -  En définissant des noms de police/couleur hors thème :
font->set_Name(u"Arial");
font->set_Color(System::Drawing::Color::get_Blue());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFont());
ASSERT_EQ(u"Arial", font->get_Name());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontAscii());
ASSERT_EQ(u"Arial", font->get_NameAscii());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontBi());
ASSERT_EQ(u"Arial", font->get_NameBi());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontFarEast());
ASSERT_EQ(u"Arial", font->get_NameFarEast());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontOther());
ASSERT_EQ(u"Arial", font->get_NameOther());

ASSERT_EQ(Aspose::Words::Themes::ThemeColor::None, font->get_ThemeColor());
ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), font->get_Color().ToArgb());
```


Montre comment créer et utiliser un style thématisé.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Créez un style avec les propriétés de police du thème.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"ThemedStyle");
style->get_Font()->set_ThemeFont(Aspose::Words::Themes::ThemeFont::Major);
style->get_Font()->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent5);
style->get_Font()->set_TintAndShade(0.3);

builder->get_ParagraphFormat()->set_StyleName(u"ThemedStyle");
builder->Writeln(u"Text with themed style");
```

## Voir aussi

* Namespace [Aspose::Words::Themes](../)
* Library [Aspose.Words for C++](../../)
