---
title: FontSettings
second_title: Aspose.Words for C++ API Reference
description: Specifies font settings for a document.
type: docs
weight: 118
url: /cpp/aspose.words.fonts/fontsettings/
---
## FontSettings class


Specifies font settings for a document.

```cpp
class FontSettings : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [FontSettings](./fontsettings/)() |  |
| static [get_DefaultInstance](./get_defaultinstance/)() | Static default font settings. |
| [get_FallbackSettings](./get_fallbacksettings/)() const | [Settings](../../aspose.words.settings/) related to font fallback mechanism. |
| [get_SubstitutionSettings](./get_substitutionsettings/)() const | [Settings](../../aspose.words.settings/) related to font substitution mechanism. |
| [GetFontsSources](./getfontssources/)() | Gets a copy of the array that contains the list of sources where Aspose.Words looks for TrueType fonts. |
| [ResetFontSources](./resetfontsources/)() | Resets the fonts sources to the system default. |
| [SaveSearchCache](./savesearchcache/)(const System::SharedPtr\<System::IO::Stream\>\&) | Saves the font search cache to the stream. |
| [SetFontsFolder](./setfontsfolder/)(const System::String\&, bool) | Sets the folder where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. This is a shortcut to **SetFontsFolders()** for setting only one font directory. |
| [SetFontsFolders](./setfontsfolders/)(const System::ArrayPtr\<System::String\>\&, bool) | Sets the folders where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. |
| [SetFontsSources](./setfontssources/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&) | Sets the sources where Aspose.Words looks for TrueType fonts when rendering documents or embedding fonts. |
| [SetFontsSources](./setfontssources/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Fonts::FontSourceBase\>\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Sets the sources where Aspose.Words looks for TrueType fonts and additionally loads previously saved font search cache. |

Aspose.Words uses font settings to resolve the fonts in the document. [Fonts](../) are resolved mostly when building document layout or rendering to fixed page formats. But when loading some formats, Aspose.Words also may require to resolve the fonts. For example, when loading HTML documents Aspose.Words may resolve the fonts to perform font fallback. So it is recommended that you set the font settings in [LoadOptions](../../aspose.words.loading/loadoptions/) when loading the document. Or at least before building the layout or rendering the document to the fixed-page format.

By default all documents uses single static font settings instance. It could be accessed by [DefaultInstance](./get_defaultinstance/) property.

Changing font settings is safe at any time from any thread. But it is recommended that you do not change the font settings while processing some documents which uses this settings. This can lead to the fact that the same font will be resolved differently in different parts of the document.

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

