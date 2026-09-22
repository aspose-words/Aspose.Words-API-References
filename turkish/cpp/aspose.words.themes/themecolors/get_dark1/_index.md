---
title: "Aspose::Words::Themes::ThemeColors::get_Dark1 yöntemi"
linktitle: "get_Dark1"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Themes::ThemeColors::get_Dark1 yöntemi. C++'ta Dark 1 rengini belirtir."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.themes/themecolors/get_dark1/
---
## ThemeColors::get_Dark1 method


Dark 1 rengini belirtir.

```cpp
System::Drawing::Color Aspose::Words::Themes::ThemeColors::get_Dark1()
```


## Örnekler



Temalar için özel renkler ve yazı tipleri ayarlama yöntemini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Theme colors.docx");

// \"Theme\" nesnesi, belge temasına, varsayılan yazı tipleri ve renklerin kaynağına erişim sağlar.
System::SharedPtr<Aspose::Words::Themes::Theme> theme = doc->get_Theme();

// \"Heading 1\" ve \"Subtitle\" gibi bazı stiller bu yazı tiplerini miras alacaktır.
theme->get_MajorFonts()->set_Latin(u"Courier New");
theme->get_MinorFonts()->set_Latin(u"Agency FB");

// Diğer diller de bu temada kendi özel yazı tiplerine sahip olabilir.
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_EastAsian());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_EastAsian());

// \"Colors\" özelliği Microsoft Word'den renk paletini içerir,
// gölgelendirme veya yazı tipi rengi değiştirildiğinde ortaya çıkar.
// Microsoft Word'de kolay erişim sağlamak için renk paletine özel renkler uygulayın
// örneğin, \"Home\" -> \"Font\" -> \"Font Color\" üzerinden yazı tipi rengini değiştirdiğimizde,
// veya bir şekil ekleyip, ardından \"Shape Format\" -> \"Shape Styles\" üzerinden ona renk atadığınızda.
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

// Bağlantıların tıklanmış ve tıklanmamış durumlarında özel renkler uygulayın.
colors->set_Hyperlink(System::Drawing::Color::get_Black());
colors->set_FollowedHyperlink(System::Drawing::Color::get_Gray());

doc->Save(get_ArtifactsDir() + u"Themes.CustomColorsAndFonts.docx");
```

## Ayrıca Bakınız

* Class [ThemeColors](../)
* Namespace [Aspose::Words::Themes](../../)
* Library [Aspose.Words for C++](../../../)
