---
title: get_UseTargetMachineFonts
second_title: Aspose.Words for C++ API Reference
description: Flag indicates whether fonts from target machine must be used to display the document. If this flag is set to true, FontFormat and ExportEmbeddedFonts properties do not have effect, also ResourceSavingCallback is not fired for fonts. Default is false.
type: docs
weight: 248
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
auto doc = MakeObject<Document>(MyDir + u"Bullet points with alternative font.docx");

auto saveOptions = MakeObject<HtmlFixedSaveOptions>();
saveOptions->set_ExportEmbeddedCss(true);
saveOptions->set_UseTargetMachineFonts(useTargetMachineFonts);
saveOptions->set_FontFormat(ExportFontFormat::Ttf);
saveOptions->set_ExportEmbeddedFonts(false);

doc->Save(ArtifactsDir + u"HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlFixedSaveOptions.UsingMachineFonts.html");

if (useTargetMachineFonts)
{
    ASSERT_FALSE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face")->get_Success());
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(
                    outDocContents, String(u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], ") +
                                        u"url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; }")
                    ->get_Success());
}
```

## See Also

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
