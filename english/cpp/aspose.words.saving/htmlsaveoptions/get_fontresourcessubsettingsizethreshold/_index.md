---
title: Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold method
linktitle: get_FontResourcesSubsettingSizeThreshold
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold method. Controls which font resources need subsetting when saving to HTML, MHTML or EPUB. Default is %0 in C++.'
type: docs
weight: 31000
url: /cpp/aspose.words.saving/htmlsaveoptions/get_fontresourcessubsettingsizethreshold/
---
## HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold method


Controls which font resources need subsetting when saving to HTML, MHTML or EPUB. Default is **%0**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold() const
```

## Remarks


[ExportFontResources](../get_exportfontresources/) allows exporting fonts as subsidiary files or as parts of the output package. If the document uses many fonts, especially with large number of glyphs, then output size can grow significantly. [Font](../../../aspose.words/font/) subsetting reduces the size of the exported font resource by filtering out glyphs that are not used by the current document.

[Font](../../../aspose.words/font/) subsetting works as follows:

* By default, all exported fonts are subsetted.
* Setting [FontResourcesSubsettingSizeThreshold](./) to a positive value instructs Aspose.Words to subset fonts which file size is larger than the specified value.
* Setting the property to **MaxValue** suppresses font subsetting.



**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## Examples



Shows how to work with font subsetting. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Courier New");
builder->Writeln(u"Hello world!");

// When we save the document to HTML, we can pass a SaveOptions object configure font subsetting.
// Suppose we set the "ExportFontResources" flag to "true" and also name a folder in the "FontsFolder" property.
// In that case, the saving operation will create that folder and place a .ttf file inside
// that folder for each font that our document uses.
// Each .ttf file will contain that font's entire glyph set,
// which may potentially result in a very large file that accompanies the document.
// When we apply subsetting to a font, its exported raw data will only contain the glyphs that the document is
// using instead of the entire glyph set. If the text in our document only uses a small fraction of a font's
// glyph set, then subsetting will significantly reduce our output documents' size.
// We can use the "FontResourcesSubsettingSizeThreshold" property to define a .ttf file size, in bytes.
// If an exported font creates a size bigger file than that, then the save operation will apply subsetting to that font.
// Setting a threshold of 0 applies subsetting to all fonts,
// and setting it to "int.MaxValue" effectively disables subsetting.
System::String fontsFolder = get_ArtifactsDir() + u"HtmlSaveOptions.FontSubsetting.Fonts";

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportFontResources(true);
options->set_FontsFolder(fontsFolder);
options->set_FontResourcesSubsettingSizeThreshold(fontResourcesSubsettingSizeThreshold);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.FontSubsetting.html", options);

System::ArrayPtr<System::String> fontFileNames = System::IO::Directory::GetFiles(fontsFolder)->LINQ_Where(static_cast<System::Func<System::String, bool>>(static_cast<std::function<bool(System::String s)>>([](System::String s) -> bool
{
    return s.EndsWith(u".ttf");
})))->LINQ_ToArray();

ASSERT_EQ(3, fontFileNames->get_Length());

for (System::String filename : fontFileNames)
{
    // By default, the .ttf files for each of our three fonts will be over 700MB.
    // Subsetting will reduce them all to under 30MB.
    auto fontFileInfo = System::MakeObject<System::IO::FileInfo>(filename);

    ASSERT_TRUE(fontFileInfo->get_Length() > 700000 || fontFileInfo->get_Length() < 30000);
    ASSERT_TRUE(System::Math::Max(fontResourcesSubsettingSizeThreshold, 30000) > System::MakeObject<System::IO::FileInfo>(filename)->get_Length());
}
```

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
