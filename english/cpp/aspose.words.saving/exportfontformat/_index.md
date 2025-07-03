---
title: Aspose::Words::Saving::ExportFontFormat enum
linktitle: ExportFontFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ExportFontFormat enum. Indicates the format that is used to export fonts while rendering to HTML fixed format in C++.'
type: docs
weight: 54000
url: /cpp/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enum


Indicates the format that is used to export fonts while rendering to HTML fixed format.

```cpp
enum class ExportFontFormat
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Woff | 0 | WOFF (Web Open [Font](../../aspose.words/font/) Format). |
| Ttf | 1 | TTF (TrueType [Font](../../aspose.words/font/) format). |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
