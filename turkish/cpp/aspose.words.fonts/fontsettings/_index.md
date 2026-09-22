---
title: "Aspose::Words::Fonts::FontSettings class"
linktitle: "FontSettings"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontSettings sınıfı. Bir belge için yazı tipi ayarlarını belirtir. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.fonts/fontsettings/
---
## FontSettings class


Bir belge için yazı tipi ayarlarını belirtir. Daha fazla bilgi için, [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) dokümantasyon makalesini ziyaret edin.

```cpp
class FontSettings : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [FontSettings](./fontsettings/)() |  |
| static [get_DefaultInstance](./get_defaultinstance/)() | Statik varsayılan yazı tipi ayarları. |
| [get_FallbackSettings](./get_fallbacksettings/)() const | Yazı tipi geri dönüş mekanizmasıyla ilgili [Settings](../../aspose.words.settings/) |
| [get_SubstitutionSettings](./get_substitutionsettings/)() const | Yazı tipi ikame mekanizmasıyla ilgili [Settings](../../aspose.words.settings/) |
| [GetFontsSources](./getfontssources/)() | Aspose.Words'ün TrueType yazı tiplerini aradığı kaynakların listesini içeren dizinin bir kopyasını alır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ResetFontSources](./resetfontsources/)() | Yazı tipi kaynaklarını sistem varsayılanına sıfırlar. |
| [SaveSearchCache](./savesearchcache/)(const System::SharedPtr\<System::IO::Stream\>\&) | Yazı tipi arama önbelleğini akışa kaydeder. |
| [SetFontsFolder](./setfontsfolder/)(const System::String\&, bool) | Aspose.Words'ün belgeleri işlerken veya yazı tiplerini gömerek TrueType yazı tiplerini aradığı klasörü ayarlar. Bu, yalnızca bir yazı tipi dizini ayarlamak için [SetFontsFolders()](../) kısayoludur. |
| [SetFontsFolders](./setfontsfolders/)(const System::ArrayPtr\<System::String\>\&, bool) | Aspose.Words'ün belgeleri işlerken veya yazı tiplerini gömerek TrueType yazı tiplerini aradığı klasörleri ayarlar. |
| [SetFontsSources](./setfontssources/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&) | Aspose.Words'ün belgeleri işlerken veya yazı tiplerini gömerek TrueType yazı tiplerini aradığı kaynakları ayarlar. |
| [SetFontsSources](./setfontssources/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Aspose.Words'ün TrueType yazı tiplerini aradığı kaynakları ayarlar ve ayrıca daha önce kaydedilmiş yazı tipi arama önbelleğini yükler. |
| static [Type](./type/)() |  |
## Açıklamalar


Aspose.Words belge içindeki yazı tiplerini çözmek için yazı tipi ayarlarını kullanır. [Fonts](../) çoğunlukla belge düzeni oluşturulurken veya sabit sayfa biçimlerine render edilirken çözülür. Ancak bazı biçimler yüklenirken, Aspose.Words da yazı tiplerini çözmek zorunda kalabilir. Örneğin, HTML belgeleri yüklenirken Aspose.Words, yazı tipi geri dönüşünü gerçekleştirmek için yazı tiplerini çözebilir. Bu nedenle, belgeyi yüklerken [LoadOptions](../../aspose.words.loading/loadoptions/) içinde yazı tipi ayarlarını belirlemeniz önerilir. Ya da en azından düzeni oluştururken veya belgeyi sabit sayfa biçimine render etmeden önce.

Varsayılan olarak tüm belgeler tek bir statik yazı tipi ayarı örneği kullanır. Bu, [DefaultInstance](./get_defaultinstance/) özelliğiyle erişilebilir.

Yazı tipi ayarlarını değiştirmek herhangi bir zamanda ve herhangi bir iş parçacığından güvenlidir. Ancak, bu ayarları kullanan bazı belgeleri işlerken yazı tipi ayarlarını değiştirmemeniz önerilir. Bu, aynı yazı tipinin belgenin farklı bölümlerinde farklı şekilde çözümlenmesine neden olabilir.

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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
