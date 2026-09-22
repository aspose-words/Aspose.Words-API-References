---
title: "Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName method"
linktitle: "get_DefaultFontName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName method. Varsayılan yazı tipi adını alır veya ayarlar C++'ta."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fonts/defaultfontsubstitutionrule/get_defaultfontname/
---
## DefaultFontSubstitutionRule::get_DefaultFontName method


Varsayılan yazı tipi adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName()
```

## Açıklamalar


Varsayılan değer 'Times New Roman'.

## Örnekler



Varsayılan bir yazı tipinin nasıl belirtileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Arvo");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// Belge tarafından kullanılan yazı tipi kaynakları "Arial" yazı tipini içeriyor, ancak "Arvo" yazı tipini içermiyor.
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// "DefaultFontName" özelliğini "Courier New" olarak ayarlayın,
// belgeyi işlerken, başka bir yazı tipi mevcut olmadığında her durumda bu yazı tipini uygular.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Courier New");

ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// Aspose.Words artık eksik yazı tiplerinin yerine varsayılan yazı tipini tüm işleme çağrıları sırasında kullanacaktır.
doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontName.pdf");
```


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

* Class [DefaultFontSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
