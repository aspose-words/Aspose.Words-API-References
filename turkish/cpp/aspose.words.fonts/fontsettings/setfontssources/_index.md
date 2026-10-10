---
title: "Aspose::Words::Fonts::FontSettings::SetFontsSources metodu"
linktitle: "SetFontsSources"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontSettings::SetFontsSources metodu. Aspose.Words'in belgeleri işlerken veya C++'ta yazı tiplerini gömerek TrueType yazı tiplerini aradığı kaynakları ayarlar."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.fonts/fontsettings/setfontssources/
---
## FontSettings::SetFontsSources(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&) method


Aspose.Words'ün belgeleri işlerken veya yazı tiplerini gömerek TrueType yazı tiplerini aradığı kaynakları ayarlar.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsSources(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> &sources)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sources | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\& | TrueType yazı tiplerini içeren kaynakların bir dizisi. |
## Açıklamalar


Varsayılan olarak, Aspose.Words sistemde yüklü yazı tiplerini arar.

Bu özelliği ayarlamak, daha önce yüklenen tüm yazı tiplerinin önbelleğini sıfırlar.

## Örnekler



Mevcut yazı tipi kaynaklarımıza bir yazı tipi kaynağı nasıl eklenir gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");
builder->get_Font()->set_Name(u"Junction Light");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> originalFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, originalFontSources->get_Length());

ASSERT_TRUE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// Varsayılan yazı tipi kaynağı, belgemizde kullandığımız iki yazı tipini eksik.
// Bu belgeyi kaydettiğimizde, Aspose.Words erişilemeyen yazı tipleriyle biçimlendirilmiş tüm metne yedek yazı tipleri uygulayacaktır.
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

// Yazı tipleri içeren bir klasörden bir yazı tipi kaynağı oluşturun.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true);

// Orijinal yazı tipi kaynaklarını ve ayrıca özel yazı tiplerimizi içeren yeni bir yazı tipi kaynağı dizisi uygulayın.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> updatedFontSources = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({originalFontSources[0], folderFontSource});
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(updatedFontSources);

// Belgeyi PDF'ye dönüştürmeden önce Aspose.Words'ün tüm gerekli yazı tiplerine erişimi olduğunu doğrulayın.
updatedFontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_TRUE(updatedFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));
ASSERT_TRUE(updatedFontSources[1]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_TRUE(updatedFontSources[1]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

doc->Save(get_ArtifactsDir() + u"FontSettings.AddFontSource.pdf");

// Orijinal yazı tipi kaynaklarını geri yükleyin.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```

## Ayrıca Bakınız

* Class [FontSourceBase](../../fontsourcebase/)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontSettings::SetFontsSources(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Aspose.Words'ün TrueType yazı tiplerini aradığı kaynakları ayarlar ve ayrıca daha önce kaydedilmiş yazı tipi arama önbelleğini yükler.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsSources(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> &sources, const System::SharedPtr<System::IO::Stream> &cacheInputStream)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sources | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\& | TrueType yazı tiplerini içeren kaynakların bir dizisi. |
| cacheInputStream | const System::SharedPtr\<System::IO::Stream\>\& | Kaydedilmiş yazı tipi arama önbelleği içeren giriş akışı. |
## Açıklamalar


[Loading](../../../aspose.words.loading/) previously saved font search cache will speed up the font cache initialization process. It is especially useful when access to font sources is complicated (e.g. when fonts are loaded via network).

Yazı tipi arama önbelleğini kaydederken ve yüklerken, sağlanan kaynaklardaki yazı tipleri önbellek anahtarıyla tanımlanır. [SystemFontSource](../../systemfontsource/) ve [FolderFontSource](../../folderfontsource/) içindeki yazı tipleri için önbellek anahtarı, yazı tipi dosyasının yoludur. [MemoryFontSource](../../memoryfontsource/) ve [StreamFontSource](../../streamfontsource/) için önbellek anahtarı sırasıyla [CacheKey](../../memoryfontsource/get_cachekey/) ve [CacheKey](../../streamfontsource/get_cachekey/) özelliklerinde tanımlanır. [FileFontSource](../../filefontsource/) için önbellek anahtarı, [CacheKey](../../filefontsource/get_cachekey/) özelliği ya da [CacheKey](../../filefontsource/get_cachekey/) **null** ise bir dosya yolu olabilir.

Önbellek yüklenirken, önbelleğin kaydedildiği zamankiyle aynı yazı tipi kaynaklarını sağlamak şiddetle tavsiye edilir. Yazı tipi kaynaklarındaki (ör. yeni yazı tipleri eklemek, yazı tipi dosyalarını taşımak veya önbellek anahtarını değiştirmek) herhangi bir değişiklik, Aspose.Words tarafından yazı tipinin hatalı çözülmesine neden olabilir.

## Ayrıca Bakınız

* Class [FontSourceBase](../../fontsourcebase/)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
