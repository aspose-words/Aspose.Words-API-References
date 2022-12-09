---
title: get_ExportFontResources
second_title: Aspose.Words for C++ API Reference
description: Specifies whether font resources should be exported to HTML, MHTML or EPUB. Default is false.
type: docs
weight: 196
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exportfontresources/
---
## HtmlSaveOptions::get_ExportFontResources method


Specifies whether font resources should be exported to HTML, MHTML or EPUB. Default is **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources() const
```

## Remarks


Exporting font resources allows for consistent document rendering independent of the fonts available in a given user's environment.

If [ExportFontResources](./) is set to **true**, main HTML document will refer to every font via the CSS 3 **%@font-face** at-rule and fonts will be output as separate files. When exporting to IDPF EPUB or MHTML formats, fonts will be embedded into the corresponding package along with other subsidiary files.

If [ExportFontsAsBase64](../get_exportfontsasbase64/) is set to **true**, fonts will not be saved to separate files. Instead, they will be embedded into **%@font-face** at-rules in Base64 encoding.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

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

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
