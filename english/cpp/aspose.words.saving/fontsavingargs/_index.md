---
title: FontSavingArgs
second_title: Aspose.Words for C++ API Reference
description: Provides data for the FontSaving() event.
type: docs
weight: 92
url: /cpp/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class


Provides data for the [FontSaving()](../ifontsavingcallback/fontsaving/) event.

```cpp
class FontSavingArgs : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Bold](./get_bold/)() const | Indicates whether the current font is bold. |
| [get_Document](./get_document/)() const | Gets the document object that is being saved. |
| [get_FontFamilyName](./get_fontfamilyname/)() const | Indicates the current font family name. |
| [get_FontFileName](./get_fontfilename/)() const | Gets or sets the file name (without path) where the font will be saved to. |
| [get_FontStream](./get_fontstream/)() const | Allows to specify the stream where the font will be saved to. |
| [get_IsExportNeeded](./get_isexportneeded/)() const | Allows to specify whether the current font will be exported as a font resource. Default is **true**. |
| [get_IsSubsettingNeeded](./get_issubsettingneeded/)() const | Allows to specify whether the current font will be subsetted before exporting as a font resource. |
| [get_Italic](./get_italic/)() const | Indicates whether the current font is italic. |
| [get_KeepFontStreamOpen](./get_keepfontstreamopen/)() const | Specifies whether Aspose.Words should keep the stream open or close it after saving a font. |
| [get_OriginalFileName](./get_originalfilename/)() const | Gets the original font file name with an extension. |
| [get_OriginalFileSize](./get_originalfilesize/)() const | Gets the original font file size. |
| [set_FontFileName](./set_fontfilename/)(const System::String\&) | Setter for [Aspose::Words::Saving::FontSavingArgs::get_FontFileName](./get_fontfilename/). |
| [set_FontStream](./set_fontstream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Setter for [Aspose::Words::Saving::FontSavingArgs::get_FontStream](./get_fontstream/). |
| [set_FontStream](./set_fontstream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_IsExportNeeded](./set_isexportneeded/)(bool) | Setter for [Aspose::Words::Saving::FontSavingArgs::get_IsExportNeeded](./get_isexportneeded/). |
| [set_IsSubsettingNeeded](./set_issubsettingneeded/)(bool) | Setter for [Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded](./get_issubsettingneeded/). |
| [set_KeepFontStreamOpen](./set_keepfontstreamopen/)(bool) | Setter for [Aspose::Words::Saving::FontSavingArgs::get_KeepFontStreamOpen](./get_keepfontstreamopen/). |

When Aspose.Words saves a document to HTML or related formats and [ExportFontResources](../htmlsaveoptions/get_exportfontresources/) is set to **true**, it saves each font subject for export into a separate file.

[FontSavingArgs](./) controls whether particular font resource should be exported and how.

[FontSavingArgs](./) also allows to redefine how font file names are generated or to completely circumvent saving of fonts into files by providing your own stream objects.

To decide whether to save a particular font resource, use the [IsExportNeeded](./get_isexportneeded/) property.

To save fonts into streams instead of files, use the [FontStream](./get_fontstream/) property.

## Examples




Shows how to define custom logic for exporting fonts when saving to HTML. 
```cpp
void SaveExportedFonts()
{
    auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

    // Configure a SaveOptions object to export fonts to separate files.
    // Set a callback that will handle font saving in a custom manner.
    auto options = MakeObject<HtmlSaveOptions>();
    options->set_ExportFontResources(true);
    options->set_FontSavingCallback(MakeObject<ExHtmlSaveOptions::HandleFontSaving>());

    // The callback will export .ttf files and save them alongside the output document.
    doc->Save(ArtifactsDir + u"HtmlSaveOptions.SaveExportedFonts.html", options);

    std::function<bool(String s)> endsWithTtf = [](String s)
    {
        return s.EndsWith(u".ttf");
    };

    for (String fontFilename : System::Array<String>::FindAll(System::IO::Directory::GetFiles(ArtifactsDir), endsWithTtf))
    {
        std::cout << fontFilename << std::endl;
    }

}

class HandleFontSaving : public IFontSavingCallback
{
private:
    void FontSaving(SharedPtr<FontSavingArgs> args) override
    {
        std::cout << "Font:\t" << args->get_FontFamilyName();
        if (args->get_Bold())
        {
            std::cout << ", bold";
        }
        if (args->get_Italic())
        {
            std::cout << ", italic";
        }
        std::cout << "\nSource:\t" << args->get_OriginalFileName() << ", " << args->get_OriginalFileSize() << " bytes\n" << std::endl;

        // We can also access the source document from here.
        ASSERT_TRUE(args->get_Document()->get_OriginalFileName().EndsWith(u"Rendering.docx"));

        ASSERT_TRUE(args->get_IsExportNeeded());
        ASSERT_TRUE(args->get_IsSubsettingNeeded());

        // There are two ways of saving an exported font.
        // 1 -  Save it to a local file system location:
        args->set_FontFileName(args->get_OriginalFileName().Split(MakeArray<char16_t>({System::IO::Path::DirectorySeparatorChar}))->LINQ_Last());

        // 2 -  Save it to a stream:
        args->set_FontStream(MakeObject<System::IO::FileStream>(
            ArtifactsDir + args->get_OriginalFileName().Split(MakeArray<char16_t>({System::IO::Path::DirectorySeparatorChar}))->LINQ_Last(),
            System::IO::FileMode::Create));
        ASSERT_FALSE(args->get_KeepFontStreamOpen());
    }
};
```

