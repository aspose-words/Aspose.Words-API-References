---
title: SetFontsFolder
second_title: Aspose.Words for C++ API Reference
description: Sets the folder where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. This is a shortcut to SetFontsFolders() for setting only one font directory.
type: docs
weight: 92
url: /cpp/aspose.words.fonts/fontsettings/setfontsfolder/
---
## FontSettings::SetFontsFolder method


Sets the folder where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. This is a shortcut to [SetFontsFolders()](../) for setting only one font directory.

```cpp
void Aspose::Words::Fonts::FontSettings::SetFontsFolder(const System::String &fontFolder, bool recursive)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fontFolder | const System::String\& | The folder that contains TrueType fonts. |
| recursive | bool | True to scan the specified folders for fonts recursively. |

## Examples



Shows how to set a font source directory. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arvo");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

// Our font sources do not contain the font that we have used for text in this document.
// If we use these font settings while rendering this document,
// Aspose.Words will apply a fallback font to text which has a font that Aspose.Words cannot locate.
ArrayPtr<SharedPtr<FontSourceBase>> originalFontSources = FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, originalFontSources->get_Length());
ASSERT_TRUE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Arial"; }));

// The default font sources are missing the two fonts that we are using in this document.
ASSERT_FALSE(originalFontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Arvo"; }));
ASSERT_FALSE(
    originalFontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Amethysta"; }));

// Use the "SetFontsFolder" method to set a directory which will act as a new font source.
// Pass "false" as the "recursive" argument to include fonts from all the font files that are in the directory
// that we are passing in the first argument, but not include any fonts in any of that directory's subfolders.
// Pass "true" as the "recursive" argument to include all font files in the directory that we are passing
// in the first argument, as well as all the fonts in its subdirectories.
FontSettings::get_DefaultInstance()->SetFontsFolder(FontsDir, recursive);

ArrayPtr<SharedPtr<FontSourceBase>> newFontSources = FontSettings::get_DefaultInstance()->GetFontsSources();

ASSERT_EQ(1, newFontSources->get_Length());
ASSERT_FALSE(newFontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Arial"; }));
ASSERT_TRUE(newFontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Arvo"; }));

// The "Amethysta" font is in a subfolder of the font directory.
if (recursive)
{
    ASSERT_EQ(25, newFontSources[0]->GetAvailableFonts()->get_Count());
    ASSERT_TRUE(newFontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Amethysta"; }));
}
else
{
    ASSERT_EQ(18, newFontSources[0]->GetAvailableFonts()->get_Count());
    ASSERT_FALSE(newFontSources[0]->GetAvailableFonts()->LINQ_Any([](SharedPtr<PhysicalFontInfo> f) { return f->get_FullFontName() == u"Amethysta"; }));
}

doc->Save(ArtifactsDir + u"FontSettings.SetFontsFolder.pdf");

// Restore the original font sources.
FontSettings::get_DefaultInstance()->SetFontsSources(originalFontSources);
```

## See Also

* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words](../../../)
