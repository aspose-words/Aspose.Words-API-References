---
title: "Aspose::Words::Document::get_FontSettings yöntemi"
linktitle: "get_FontSettings"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_FontSettings yöntemi. C++'ta belge yazı tipi ayarlarını alır veya ayarlar."
type: docs
weight: 25000
url: /tr/cpp/aspose.words/document/get_fontsettings/
---
## Document::get_FontSettings method


Belge yazı tipi ayarlarını alır veya ayarlar.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Document::get_FontSettings() const
```

## Açıklamalar


Bu özellik, belge başına yazı tipi ayarlarını belirtmeye izin verir. **null** olarak ayarlanırsa, varsayılan sabit yazı tipi ayarları [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/) kullanılacaktır.

Varsayılan değer **null**'dır.

## Örnekler



Yazı tipi değiştirme kurallarının nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// Varsayılan yazı tipi kaynakları, belgenin kullandığı ilk yazı tipini içerir.
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// İkinci yazı tipi, "Amethysta", mevcut değil.
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// Yazı tipi değiştirme tablosunu yapılandırabiliriz, bu tablo belirler
// hangi yazı tiplerinin Aspose.Words tarafından mevcut olmayan yazı tipleri için yedek olarak kullanılacağını.
// "Amethysta" için iki yedek yazı tipi ayarlayın: "Arvo" ve "Courier New".
// İlk yedek mevcut değilse, Aspose.Words ikinci yedeği kullanmayı dener ve bu şekilde devam eder.
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->SetSubstitutes(u"Amethysta", System::MakeArray<System::String>({u"Arvo", u"Courier New"}));

// "Amethysta" mevcut değil ve değiştirme kuralı, yedek olarak kullanılacak ilk yazı tipinin "Arvo" olduğunu belirtir.
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// "Arvo" da mevcut değil, ancak "Courier New" mevcut.
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// Çıktı belgesi, "Amethysta" yazı tipini kullanan metni "Courier New" ile biçimlendirilmiş olarak gösterecek.
doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitution.pdf");
```

## Ayrıca Bakınız

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
