---
title: "Aspose::Words::Fonts::FontSettings::SetFontsFolder method"
linktitle: "SetFontsFolder"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontSettings::SetFontsFolder method. Aspose.Words'ün belgeleri işlerken veya fontları gömerek TrueType fontlarını aradığı klasörü ayarlar. Bu, C++'da yalnızca bir font dizini ayarlamak için SetFontsFolders() kısayoludur."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.fonts/fontsettings/setfontsfolder/
---
## FontSettings::SetFontsFolder method


Aspose.Words'ün belgeleri işlerken veya yazı tiplerini gömerek TrueType yazı tiplerini aradığı klasörü ayarlar. Bu, yalnızca bir yazı tipi dizini ayarlamak için [SetFontsFolders()](../) kısayoludur.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsFolder(const System::String &fontFolder, bool recursive)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontFolder | const System::String\& | TrueType yazı tiplerini içeren klasör. |
| özyinelemeli | bool | Belirtilen klasörlerdeki yazı tiplerini özyinelemeli olarak taramak için True. |

## Örnekler



Bir yazı tipi kaynağı dizini nasıl ayarlanır gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arvo");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

// Yazı tipi kaynaklarımız bu belgede metin için kullandığımız yazı tipini içermiyor.
// Bu belgeyi işlerken bu yazı tipi ayarlarını kullanırsak,
// Aspose.Words, bulunamayan bir yazı tipine sahip metne bir yedek yazı tipi uygulayacaktır.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> originalFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, originalFontSources->get_Length());
ASSERT_TRUE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// Varsayılan yazı tipi kaynakları bu belgede kullandığımız iki yazı tipini eksik.
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// "SetFontsFolder" metodunu, yeni bir yazı tipi kaynağı olarak işlev görecek bir dizini ayarlamak için kullanın.
// "recursive" argümanı olarak "false" geçirerek dizindeki tüm yazı tipi dosyalarından yazı tiplerini dahil edin
// ilk argümanda geçirdiğimiz, ancak o dizinin alt klasörlerindeki hiçbir yazı tipini dahil etmeyen
// "recursive" argümanı olarak "true" geçirerek geçirdiğimiz dizindeki tüm yazı tipi dosyalarını dahil edin
// ilk argümanda, ayrıca alt dizinlerindeki tüm yazı tiplerini de.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsFolder(get_FontsDir(), recursive);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> newFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, newFontSources->get_Length());
ASSERT_FALSE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_TRUE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// "Amethysta" yazı tipi, yazı tipi dizininin bir alt klasöründe bulunuyor.
if (recursive)
{
    ASSERT_EQ(30, newFontSources[0]->GetAvailableFonts()->get_Count());
    ASSERT_TRUE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
    {
        return f->get_FullFontName() == u"Amethysta";
    }))));
}
else
{
    ASSERT_EQ(18, newFontSources[0]->GetAvailableFonts()->get_Count());
    ASSERT_FALSE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
    {
        return f->get_FullFontName() == u"Amethysta";
    }))));
}

doc->Save(get_ArtifactsDir() + u"FontSettings.SetFontsFolder.pdf");

// Orijinal yazı tipi kaynaklarını geri yükleyin.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```

## Ayrıca Bakınız

* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
