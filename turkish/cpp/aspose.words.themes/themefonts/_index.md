---
title: "Aspose::Words::Themes::ThemeFonts class"
linktitle: "ThemeFonts"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Themes::ThemeFonts sınıfı. Yazı tipi şemasındaki yazı tiplerinin bir koleksiyonunu temsil eder ve Latin, EastAsian ve ComplexScript gibi farklı diller için farklı yazı tipleri belirtmeye olanak tanır. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.themes/themefonts/
---
## ThemeFonts class


Yazı tipi şemasındaki yazı tiplerinin bir koleksiyonunu temsil eder ve farklı diller için farklı yazı tipleri belirtmeye olanak tanır: [Latin](./get_latin/), [EastAsian](./get_eastasian/) ve [ComplexScript](./get_complexscript/). Daha fazla bilgi için [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/) belge makalesini ziyaret edin.

```cpp
class ThemeFonts : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_ComplexScript](./get_complexscript/)() | ComplexScript karakterleri için yazı tipi adını belirtir. |
| [get_EastAsian](./get_eastasian/)() | EastAsian karakterleri için yazı tipi adını belirtir. |
| [get_Latin](./get_latin/)() | Latin karakterleri için yazı tipi adını belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ComplexScript](./set_complexscript/)(const System::String\&) | Ayarlayıcı: [Aspose::Words::Themes::ThemeFonts::get_ComplexScript](./get_complexscript/). |
| [set_EastAsian](./set_eastasian/)(const System::String\&) | Ayarlayıcı: [Aspose::Words::Themes::ThemeFonts::get_EastAsian](./get_eastasian/). |
| [set_Latin](./set_latin/)(const System::String\&) | Ayarlayıcı: [Aspose::Words::Themes::ThemeFonts::get_Latin](./get_latin/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Themes](../)
* Library [Aspose.Words for C++](../../)
