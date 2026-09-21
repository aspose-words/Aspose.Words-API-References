---
title: "Aspose::Words::Fonts::FontSettings::SetFontsSources metod"
linktitle: "SetFontsSources"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontSettings::SetFontsSources metod. Anger källorna där Aspose.Words letar efter TrueType-teckensnitt när dokument renderas eller teckensnitt bäddas in i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words.fonts/fontsettings/setfontssources/
---
## FontSettings::SetFontsSources(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&) method


Anger källorna där Aspose.Words söker efter TrueType-teckensnitt när dokument renderas eller teckensnitt bäddas in.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsSources(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> &sources)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sources | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\& | En array av källor som innehåller TrueType-teckensnitt. |
## Anmärkningar


Som standard letar Aspose.Words efter teckensnitt som är installerade i systemet.

Att sätta denna egenskap återställer cachen för alla tidigare inlästa teckensnitt.

## Exempel



Visar hur man lägger till en teckensnittskälla till våra befintliga teckensnittskällor.
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

// Den standardteckensnittskällan saknar två av de teckensnitt som vi använder i vårt dokument.
// När vi sparar detta dokument kommer Aspose.Words att använda reservteckensnitt för all text som är formaterad med otillgängliga teckensnitt.
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

// Skapa en teckensnittskälla från en mapp som innehåller teckensnitt.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true);

// Applicera en ny array av teckensnittskällor som innehåller de ursprungliga teckensnittskällorna, samt våra egna teckensnitt.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> updatedFontSources = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({originalFontSources[0], folderFontSource});
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(updatedFontSources);

// Verifiera att Aspose.Words har åtkomst till alla nödvändiga teckensnitt innan vi renderar dokumentet till PDF.
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

// Återställ de ursprungliga teckensnittskällorna.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```

## Se även

* Class [FontSourceBase](../../fontsourcebase/)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontSettings::SetFontsSources(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Anger källorna där Aspose.Words söker efter TrueType-teckensnitt och laddar dessutom tidigare sparad teckensnittssökcache.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsSources(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> &sources, const System::SharedPtr<System::IO::Stream> &cacheInputStream)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sources | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\& | En array av källor som innehåller TrueType-teckensnitt. |
| cacheInputStream | const System::SharedPtr\<System::IO::Stream\>\& | Inmatningsström med sparad teckensnittssökcache. |
## Anmärkningar


[Loading](../../../aspose.words.loading/) previously saved font search cache will speed up the font cache initialization process. It is especially useful when access to font sources is complicated (e.g. when fonts are loaded via network).

När du sparar och laddar teckensnittssökcachen identifieras teckensnitt i de angivna källorna via cache-nyckeln. För teckensnitten i [SystemFontSource](../../systemfontsource/) och [FolderFontSource](../../folderfontsource/) är cache-nyckeln sökvägen till teckensnittsfilen. För [MemoryFontSource](../../memoryfontsource/) och [StreamFontSource](../../streamfontsource/) definieras cache-nyckeln i egenskaperna [CacheKey](../../memoryfontsource/get_cachekey/) respektive [CacheKey](../../streamfontsource/get_cachekey/). För [FileFontSource](../../filefontsource/) är cache-nyckeln antingen egenskapen [CacheKey](../../filefontsource/get_cachekey/) eller en filsökväg om [CacheKey](../../filefontsource/get_cachekey/) är **null**.

Det rekommenderas starkt att tillhandahålla samma teckensnittskällor när cachen laddas som när den sparades. Eventuella förändringar i teckensnittskällorna (t.ex. att lägga till nya teckensnitt, flytta teckensnitts-filer eller ändra cache-nyckeln) kan leda till felaktig teckensnittsupplösning av Aspose.Words.

## Se även

* Class [FontSourceBase](../../fontsourcebase/)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
