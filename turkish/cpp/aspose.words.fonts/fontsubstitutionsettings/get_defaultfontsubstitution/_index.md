---
title: "Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution metodu"
linktitle: "get_DefaultFontSubstitution"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution metodu. C++'de varsayılan yazı tipi ikame kuralıyla ilgili ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fonts/fontsubstitutionsettings/get_defaultfontsubstitution/
---
## FontSubstitutionSettings::get_DefaultFontSubstitution method


[Settings](../../../aspose.words.settings/) related to default font substitution rule.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> & Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution() const
```


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

* Class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* Class [FontSubstitutionSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
