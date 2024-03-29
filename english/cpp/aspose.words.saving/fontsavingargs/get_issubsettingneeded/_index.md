---
title: Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded method
linktitle: get_IsSubsettingNeeded
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded method. Allows to specify whether the current font will be subsetted before exporting as a font resource in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.saving/fontsavingargs/get_issubsettingneeded/
---
## FontSavingArgs::get_IsSubsettingNeeded method


Allows to specify whether the current font will be subsetted before exporting as a font resource.

```cpp
bool Aspose::Words::Saving::FontSavingArgs::get_IsSubsettingNeeded() const
```

## Remarks


[Fonts](../../../aspose.words.fonts/) can be exported as complete original font files or subsetted to include only the characters that are used in the document. Subsetting allows to reduce the resulting font resource size.

By default, Aspose.Words decides whether to perform subsetting or not by comparing the original font file size with the one specified in [FontResourcesSubsettingSizeThreshold](../../htmlsaveoptions/get_fontresourcessubsettingsizethreshold/). You can override this behavior for individual fonts by setting the [IsSubsettingNeeded](./) property.

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

## See Also

* Class [FontSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
