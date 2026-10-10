---
title: "Aspose::Words::Themes::ThemeColor enum"
linktitle: "ThemeColor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Themes::ThemeColor enum. Belge temaları için tema renklerini belirtir. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.themes/themecolor/
---
## ThemeColor enum


Belge temaları için tema renklerini belirtir. Daha fazla bilgi edinmek için [Stiller ve Temalarla Çalışma](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/) dokümantasyon makalesini ziyaret edin.

```cpp
enum class ThemeColor
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | -1 | Renk yok. |
| Dark1 | 0 | Ana koyu renk 1. |
| Light1 | 1 | Ana açık renk 1. |
| Dark2 | 2 | Ana koyu renk 2. |
| Light2 | 3 | Ana açık renk 2. |
| Accent1 | 4 | Vurgu rengi 1. |
| Accent2 | 5 | Vurgu rengi 2. |
| Accent3 | 6 | Vurgu rengi 3. |
| Accent4 | 7 | Vurgu rengi 4. |
| Accent5 | 8 | Vurgu rengi 5. |
| Accent6 | 9 | Vurgu rengi 6. |
| Hyperlink | 10 | Köprü rengi. |
| FollowedHyperlink | 11 | Takip edilen köprü rengi. |
| Text1 | 12 | Metin rengi 1. |
| Text2 | 13 | Metin rengi 2. |
| Background1 | 14 | Arka plan rengi 1. |
| Background2 | 15 | Arka plan rengi 2. |


## Örnekler



Tema yazı tipleri ve renklerle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Diller için varsayılan olarak kullanılan yazı tiplerini tanımlayın.
doc->get_Theme()->get_MinorFonts()->set_Latin(u"Algerian");
doc->get_Theme()->get_MinorFonts()->set_EastAsian(u"Aharoni");
doc->get_Theme()->get_MinorFonts()->set_ComplexScript(u"Andalus");

System::SharedPtr<Aspose::Words::Font> font = doc->get_Styles()->idx_get(u"Normal")->get_Font();
std::cout << System::String::Format(u"Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font->get_ThemeColor(), font->get_Color()) << std::endl;

// Varsayılan değerler yerine tema yazı tipi ve rengini kullanabiliriz.
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

// Yazı tipini ve rengi sıfırlamanın birkaç yolu vardır.
// 1 -  ThemeFont.None/ThemeColor.None ayarlanarak:
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

// 2 -  Tema dışı yazı tipi/renk adları ayarlanarak:
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


Temalı stili oluşturma ve kullanma yöntemini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Tema yazı tipi özellikleriyle bazı stiller oluşturun.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"ThemedStyle");
style->get_Font()->set_ThemeFont(Aspose::Words::Themes::ThemeFont::Major);
style->get_Font()->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent5);
style->get_Font()->set_TintAndShade(0.3);

builder->get_ParagraphFormat()->set_StyleName(u"ThemedStyle");
builder->Writeln(u"Text with themed style");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Themes](../)
* Library [Aspose.Words for C++](../../)
