---
title: "Aspose::Words::Fonts::DefaultFontSubstitutionRule sınıfı"
linktitle: "DefaultFontSubstitutionRule"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::DefaultFontSubstitutionRule sınıfı. Varsayılan yazı tipi ikame kuralı. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 1000
url: /tr/cpp/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class


Varsayılan yazı tipi ikame kuralı. Daha fazla bilgi için, [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) dokümantasyon makalesini ziyaret edin.

```cpp
class DefaultFontSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_DefaultFontName](./get_defaultfontname/)() | Varsayılan yazı tipi adını alır veya ayarlar. |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Kuralın etkin olup olmadığını belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DefaultFontName](./set_defaultfontname/)(const System::String\&) | Ayarlayıcı [Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName](./get_defaultfontname/). |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Ayarlayıcı [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| static [Type](./type/)() |  |

## Örnekler



Varsayılan yazı tipi ikame kuralını nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// FontSettings içinde varsayılan ikame kuralını alın.
// Bu kural, eksik tüm yazı tiplerini "Times New Roman" ile değiştirecektir.
System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> defaultFontSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution();
ASSERT_TRUE(defaultFontSubstitutionRule->get_Enabled());
ASSERT_EQ(u"Times New Roman", defaultFontSubstitutionRule->get_DefaultFontName());

// Varsayılan yazı tipi ikamesini "Courier New" olarak ayarlayın.
defaultFontSubstitutionRule->set_DefaultFontName(u"Courier New");

// Bir belge oluşturucu kullanarak, ikamenin gerçekleştiğini görmek için sahip olmadığımız bir yazı tipinde bazı metinler ekleyin,
// ve ardından sonucu bir PDF olarak oluşturun.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Missing Font");
builder->Writeln(u"Line written in a missing font, which will be substituted with Courier New.");

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontSubstitutionRule.pdf");
```

## Ayrıca Bakınız

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
