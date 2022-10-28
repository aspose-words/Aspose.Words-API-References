---
title: SetFontsFolders
second_title: Aspose.Words for C++ API Reference
description: Sets the folders where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts.
type: docs
weight: 105
url: /cpp/aspose.words.fonts/fontsettings/setfontsfolders/
---
## FontSettings.SetFontsFolders method


Sets the folders where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsFolders(const System::ArrayPtr<System::String> &fontsFolders, bool recursive)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fontsFolders | const System::ArrayPtr\<System::String\>\& | An array of folders that contain TrueType fonts. |
| recursive | bool | True to scan the specified folders for fonts recursively. |

By default, Aspose.Words looks for fonts installed to the system.

Setting this property resets the cache of all previously loaded fonts.

## Examples




Shows how to set multiple font source directories. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");
builder->get_Font()->set_Name(u"Junction Light");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

// Our font sources do not contain the font that we have used for text in this document.
// If we use these font settings while rendering this document,
// Aspose.Words will apply a fallback font to text which has a font that Aspose.Words cannot locate.
ArrayPtr<SharedPtr<FontSourceBase>> originalFontSources = FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, originalFontSources->get_Length());
ASSERT_TRUE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Arial"; }));

// The default font sources are missing the two fonts that we are using in this document.
ASSERT_FALSE(
    originalFontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Amethysta"; }));
ASSERT_FALSE(
    originalFontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Junction Light"; }));

// Use the "SetFontsFolders" method to create a font source from each font directory that we pass as the first argument.
// Pass "false" as the "recursive" argument to include fonts from all the font files that are in the directories
// that we are passing in the first argument, but not include any fonts from any of the directories' subfolders.
// Pass "true" as the "recursive" argument to include all font files in the directories that we are passing
// in the first argument, as well as all the fonts in their subdirectories.
FontSettings::get_DefaultInstance()->SetFontsFolders(MakeArray<String>({FontsDir + u"/Amethysta", FontsDir + u"/Junction"}), recursive);

ArrayPtr<SharedPtr<FontSourceBase>> newFontSources = FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(2, newFontSources->get_Length());
ASSERT_FALSE(newFontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Arial"; }));
ASSERT_EQ(1, newFontSources[0]->GetAvailableFonts()->get_Count());
ASSERT_TRUE(newFontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Amethysta"; }));

// The "Junction" folder itself contains no font files, but has subfolders that do.
if (recursive)
{
    ASSERT_EQ(6, newFontSources[1]->GetAvailableFonts()->get_Count());
    ASSERT_TRUE(
        newFontSources[1]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Junction Light"; }));
}
else
{
    ASSERT_EQ(0, newFontSources[1]->GetAvailableFonts()->get_Count());
}

doc->Save(ArtifactsDir + u"FontSettings.SetFontsFolders.pdf");

// Restore the original font sources.
FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```

