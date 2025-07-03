---
title: Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts method
linktitle: get_UseTargetMachineFonts
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts method. Flag indicates whether fonts from target machine must be used to display the document. If this flag is set to true, FontFormat and ExportEmbeddedFonts properties do not have effect, also ResourceSavingCallback is not fired for fonts. Default is false in C++.'
type: docs
weight: 20000
url: /cpp/aspose.words.saving/htmlfixedsaveoptions/get_usetargetmachinefonts/
---
## HtmlFixedSaveOptions::get_UseTargetMachineFonts method


Flag indicates whether fonts from target machine must be used to display the document. If this flag is set to **true**, [FontFormat](../get_fontformat/) and [ExportEmbeddedFonts](../get_exportembeddedfonts/) properties do not have effect, also [ResourceSavingCallback](../get_resourcesavingcallback/) is not fired for fonts. Default is **false**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts() const
```


## Examples



Shows how use fonts only from the target machine when saving a document to HTML. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Bullet points with alternative font.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_ExportEmbeddedCss(true);
saveOptions->set_UseTargetMachineFonts(useTargetMachineFonts);
saveOptions->set_FontFormat(Aspose::Words::Saving::ExportFontFormat::Ttf);
saveOptions->set_ExportEmbeddedFonts(false);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UsingMachineFonts.html");

if (useTargetMachineFonts)
{
    ASSERT_FALSE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face")->get_Success());
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], ") + u"url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; }")->get_Success());
}
```

## See Also

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
