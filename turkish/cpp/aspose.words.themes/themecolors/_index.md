---
title: "Aspose::Words::Themes::ThemeColors sınıfı"
linktitle: "ThemeColors"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Themes::ThemeColors sınıfı. Belge temasının renk şemasını temsil eder ve on iki renk içerir. ThemeColors nesnesi altı vurgu rengi, iki koyu renk, iki açık renk ve bir bağlantı ile ziyaret edilmiş bağlantı için bir renk içerir C++'da."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.themes/themecolors/
---
## ThemeColors class


Belge temasının renk şemasını temsil eder ve on iki renk içerir. [ThemeColors](./) nesnesi altı vurgu rengi, iki koyu renk, iki açık renk ve bir bağlantı ile ziyaret edilmiş bağlantı için bir renk içerir.

```cpp
class ThemeColors : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Accent1](./get_accent1/)() | Accent 1 rengini belirtir. |
| [get_Accent2](./get_accent2/)() | Accent 2 rengini belirtir. |
| [get_Accent3](./get_accent3/)() | Accent 3 rengini belirtir. |
| [get_Accent4](./get_accent4/)() | Accent 4 rengini belirtir. |
| [get_Accent5](./get_accent5/)() | Accent 5 rengini belirtir. |
| [get_Accent6](./get_accent6/)() | Accent 6 rengini belirtir. |
| [get_Dark1](./get_dark1/)() | Dark 1 rengini belirtir. |
| [get_Dark2](./get_dark2/)() | Dark 2 rengini belirtir. |
| [get_FollowedHyperlink](./get_followedhyperlink/)() | Tıklanmış bir bağlantı için rengi belirtir. |
| [get_Hyperlink](./get_hyperlink/)() | Bir bağlantı için rengi belirtir. |
| [get_Light1](./get_light1/)() | Light 1 rengini belirtir. |
| [get_Light2](./get_light2/)() | Light 2 rengini belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Accent1](./set_accent1/)(System::Drawing::Color) | Ayarlayıcı [Aspose::Words::Themes::ThemeColors::get_Accent1](./get_accent1/). |
| [set_Accent2](./set_accent2/)(System::Drawing::Color) | Ayarlayıcı [Aspose::Words::Themes::ThemeColors::get_Accent2](./get_accent2/). |
| [set_Accent3](./set_accent3/)(System::Drawing::Color) | Ayarlayıcı [Aspose::Words::Themes::ThemeColors::get_Accent3](./get_accent3/). |
| [set_Accent4](./set_accent4/)(System::Drawing::Color) | Ayarlayıcı [Aspose::Words::Themes::ThemeColors::get_Accent4](./get_accent4/). |
| [set_Accent5](./set_accent5/)(System::Drawing::Color) | Ayarlayıcı [Aspose::Words::Themes::ThemeColors::get_Accent5](./get_accent5/). |
| [set_Accent6](./set_accent6/)(System::Drawing::Color) | Ayarlayıcı [Aspose::Words::Themes::ThemeColors::get_Accent6](./get_accent6/). |
| [set_Dark1](./set_dark1/)(System::Drawing::Color) | Ayarlayıcı [Aspose::Words::Themes::ThemeColors::get_Dark1](./get_dark1/). |
| [set_Dark2](./set_dark2/)(System::Drawing::Color) | Ayarlayıcı [Aspose::Words::Themes::ThemeColors::get_Dark2](./get_dark2/). |
| [set_FollowedHyperlink](./set_followedhyperlink/)(System::Drawing::Color) | Ayarlayıcı [Aspose::Words::Themes::ThemeColors::get_FollowedHyperlink](./get_followedhyperlink/). |
| [set_Hyperlink](./set_hyperlink/)(System::Drawing::Color) | Ayarlayıcı [Aspose::Words::Themes::ThemeColors::get_Hyperlink](./get_hyperlink/). |
| [set_Light1](./set_light1/)(System::Drawing::Color) | Ayarlayıcı [Aspose::Words::Themes::ThemeColors::get_Light1](./get_light1/). |
| [set_Light2](./set_light2/)(System::Drawing::Color) | Ayarlayıcı [Aspose::Words::Themes::ThemeColors::get_Light2](./get_light2/). |
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
