---
title: Aspose::Words::Fonts::FontSettings::SetFontsSources method
linktitle: SetFontsSources
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontSettings::SetFontsSources method. Sets the sources where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.fonts/fontsettings/setfontssources/
---
## FontSettings::SetFontsSources(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&) method


Sets the sources where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsSources(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> &sources)
```


| Parameter | Type | Description |
| --- | --- | --- |
| sources | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\& | An array of sources that contain TrueType fonts. |
## Remarks


By default, Aspose.Words looks for fonts installed to the system.

Setting this property resets the cache of all previously loaded fonts.

## Examples



Shows how to add a font source to our existing font sources. 
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

// The default font source is missing two of the fonts that we are using in our document.
// When we save this document, Aspose.Words will apply fallback fonts to all text formatted with inaccessible fonts.
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Junction Light";
}))));

// Create a font source from a folder that contains fonts.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), true);

// Apply a new array of font sources that contains the original font sources, as well as our custom fonts.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> updatedFontSources = System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({originalFontSources[0], folderFontSource});
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(updatedFontSources);

// Verify that Aspose.Words has access to all required fonts before we render the document to PDF.
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

// Restore the original font sources.
Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```

## See Also

* Class [FontSourceBase](../../fontsourcebase/)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontSettings::SetFontsSources(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Sets the sources where Aspose.Words looks for TrueType fonts and additionally loads previously saved font search cache.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsSources(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> &sources, const System::SharedPtr<System::IO::Stream> &cacheInputStream)
```


| Parameter | Type | Description |
| --- | --- | --- |
| sources | const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\& | An array of sources that contain TrueType fonts. |
| cacheInputStream | const System::SharedPtr\<System::IO::Stream\>\& | Input stream with saved font search cache. |
## Remarks


[Loading](../../../aspose.words.loading/) previously saved font search cache will speed up the font cache initialization process. It is especially useful when access to font sources is complicated (e.g. when fonts are loaded via network).

When saving and loading font search cache, fonts in the provided sources are identified via cache key. For the fonts in the [SystemFontSource](../../systemfontsource/) and [FolderFontSource](../../folderfontsource/) cache key is the path to the font file. For [MemoryFontSource](../../memoryfontsource/) and [StreamFontSource](../../streamfontsource/) cache key is defined in the [CacheKey](../../memoryfontsource/get_cachekey/) and [CacheKey](../../streamfontsource/get_cachekey/) properties respectively. For the [FileFontSource](../../filefontsource/) cache key is either [CacheKey](../../filefontsource/get_cachekey/) property or a file path if the [CacheKey](../../filefontsource/get_cachekey/) is **null**.

It is highly recommended to provide the same font sources when loading cache as at the time the cache was saved. Any changes in the font sources (e.g. adding new fonts, moving font files or changing the cache key) may lead to the inaccurate font resolving by Aspose.Words.

## See Also

* Class [FontSourceBase](../../fontsourcebase/)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
