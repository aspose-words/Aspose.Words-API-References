---
title: "Aspose::Words::Fonts::FontSettings::SetFontsFolders metodu"
linktitle: "SetFontsFolders"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontSettings::SetFontsFolders metodu. Aspose.Words'in belgeleri işlerken veya C++'ta yazı tiplerini gömerek TrueType yazı tiplerini aradığı klasörleri ayarlar."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.fonts/fontsettings/setfontsfolders/
---
## FontSettings::SetFontsFolders method


Aspose.Words'ün belgeleri işlerken veya yazı tiplerini gömerek TrueType yazı tiplerini aradığı klasörleri ayarlar.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsFolders(const System::ArrayPtr<System::String> &fontsFolders, bool recursive)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fontsFolders | const System::ArrayPtr\<System::String\>\& | TrueType yazı tiplerini içeren klasörlerin bir dizisi. |
| özyinelemeli | bool | Belirtilen klasörlerdeki yazı tiplerini özyinelemeli olarak taramak için True. |
## Açıklamalar


Varsayılan olarak, Aspose.Words sistemde yüklü yazı tiplerini arar.

Bu özelliği ayarlamak, daha önce yüklenen tüm yazı tiplerinin önbelleğini sıfırlar.

## Örnekler



Birden fazla yazı tipi kaynağı dizini nasıl ayarlanır gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");
builder->get_Font()->set_Name(u"Junction Light");
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
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

// "SetFontsFolders" metodunu, ilk argüman olarak geçirdiğimiz her yazı tipi dizininden bir yazı tipi kaynağı oluşturmak için kullanın.
// "recursive" argümanı olarak "false" geçirerek dizinlerdeki tüm yazı tipi dosyalarından yazı tiplerini dahil edin
// ilk argümanda geçirdiğimiz, ancak dizinlerin alt klasörlerindeki hiçbir yazı tipini dahil etmeyen
// "recursive" argümanı olarak "true" geçirerek geçirdiğimiz dizinlerdeki tüm yazı tipi dosyalarını dahil edin
// ilk argümanda, ayrıca alt dizinlerindeki tüm yazı tiplerini de.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsFolders(System::MakeArray<System::String>({get_FontsDir() + u"/Amethysta", get_FontsDir() + u"/Junction"}), recursive);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> newFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(2, newFontSources->get_Length());
ASSERT_FALSE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_EQ(1, newFontSources[0]->GetAvailableFonts()->get_Count());
ASSERT_TRUE(newFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// "Junction" klasörü kendisi hiçbir yazı tipi dosyası içermez, ancak içeren alt klasörleri vardır.
if (recursive)
{
    ASSERT_EQ(11, newFontSources[1]->GetAvailableFonts()->get_Count());
    ASSERT_TRUE(newFontSources[1]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
    {
        return f->get_FullFontName() == u"Junction Light";
    }))));
}
else
{
    ASSERT_EQ(0, newFontSources[1]->GetAvailableFonts()->get_Count());
}

doc->Save(get_ArtifactsDir() + u"FontSettings.SetFontsFolders.pdf");

// Orijinal yazı tipi kaynaklarını geri yükleyin.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```

## Ayrıca Bakınız

* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
