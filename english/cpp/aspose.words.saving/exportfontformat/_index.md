---
title: ExportFontFormat
second_title: Aspose.Words for C++ API Reference
description: Indicates the format that is used to export fonts while rendering to HTML fixed format.
type: docs
weight: 690
url: /cpp/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enum


Indicates the format that is used to export fonts while rendering to HTML fixed format.

### Values

| Name | Value | Description |
| --- | --- | --- |
| Woff | 0 | WOFF (Web Open [Font](../../aspose.words/font/) Format). |
| Ttf | 1 | TTF (TrueType [Font](../../aspose.words/font/) format). |


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

