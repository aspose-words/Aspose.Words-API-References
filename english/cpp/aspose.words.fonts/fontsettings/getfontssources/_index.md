---
title: GetFontsSources
second_title: Aspose.Words for C++ API Reference
description: Gets a copy of the array that contains the list of sources where Aspose.Words looks for TrueType fonts.
type: docs
weight: 53
url: /cpp/aspose.words.fonts/fontsettings/getfontssources/
---
## FontSettings.GetFontsSources method


Gets a copy of the array that contains the list of sources where Aspose.Words looks for TrueType fonts.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> Aspose::Words::Fonts::FontSettings::GetFontsSources()
```


### ReturnValue


A copy of the current font sources.

The returned value is a copy of the data that Aspose.Words uses. If you change the entries in the returned array, it will have no effect on document rendering. To specify new font sources use the **SetFontsSources()** method.

## Examples




Shows how to add a font source to our existing font sources. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");
builder->get_Font()->set_Name(u"Junction Light");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

ArrayPtr<SharedPtr<FontSourceBase>> originalFontSources = FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, originalFontSources->get_Length());

ASSERT_TRUE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Arial"; }));

// The default font source is missing two of the fonts that we are using in our document.
// When we save this document, Aspose.Words will apply fallback fonts to all text formatted with inaccessible fonts.
ASSERT_FALSE(
    originalFontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Amethysta"; }));
ASSERT_FALSE(
    originalFontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Junction Light"; }));

// Create a font source from a folder that contains fonts.
auto folderFontSource = MakeObject<FolderFontSource>(FontsDir, true);

// Apply a new array of font sources that contains the original font sources, as well as our custom fonts.
ArrayPtr<SharedPtr<FontSourceBase>> updatedFontSources = MakeArray<SharedPtr<FontSourceBase>>({originalFontSources[0], folderFontSource});
FontSettings::get_DefaultInstance()->SetFontsSources(updatedFontSources);

// Verify that Aspose.Words has access to all required fonts before we render the document to PDF.
updatedFontSources = FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_TRUE(updatedFontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Arial"; }));
ASSERT_TRUE(updatedFontSources[1]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Amethysta"; }));
ASSERT_TRUE(
    updatedFontSources[1]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Junction Light"; }));

doc->Save(ArtifactsDir + u"FontSettings.AddFontSource.pdf");

// Restore the original font sources.
FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```

