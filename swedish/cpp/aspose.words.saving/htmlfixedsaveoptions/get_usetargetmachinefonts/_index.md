---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts‑metod"
linktitle: "get_UseTargetMachineFonts"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts‑metod. Flaggan indikerar om teckensnitt från målmaskinen måste användas för att visa dokumentet. Om flaggan är satt till true har egenskaperna FontFormat och ExportEmbeddedFonts ingen effekt, och ResourceSavingCallback avfyras inte för teckensnitt. Standardvärdet är false i C++."
type: docs
weight: 20000
url: /sv/cpp/aspose.words.saving/htmlfixedsaveoptions/get_usetargetmachinefonts/
---
## HtmlFixedSaveOptions::get_UseTargetMachineFonts method


Flaggan indikerar om teckensnitt från målmaskinen måste användas för att visa dokumentet. Om flaggan är satt till **true** har [FontFormat](../get_fontformat/) och [ExportEmbeddedFonts](../get_exportembeddedfonts/) egenskaper ingen effekt, och [ResourceSavingCallback](../get_resourcesavingcallback/) avfyras inte för teckensnitt. Standardvärdet är **false**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts() const
```


## Exempel



Visar hur man använder endast typsnitt från målmaskinen när ett dokument sparas i HTML.
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

## Se även

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
