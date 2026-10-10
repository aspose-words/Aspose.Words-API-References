---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts method"
linktitle: "get_UseTargetMachineFonts"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts method. Das Flag gibt an, ob Schriftarten vom Zielrechner verwendet werden müssen, um das Dokument anzuzeigen. Wenn dieses Flag auf true gesetzt ist, haben die Eigenschaften FontFormat und ExportEmbeddedFonts keine Wirkung, außerdem wird ResourceSavingCallback für Schriftarten nicht ausgelöst. Standardwert ist false in C++."
type: docs
weight: 20000
url: /de/cpp/aspose.words.saving/htmlfixedsaveoptions/get_usetargetmachinefonts/
---
## HtmlFixedSaveOptions::get_UseTargetMachineFonts method


Das Flag gibt an, ob Schriftarten vom Zielrechner verwendet werden müssen, um das Dokument anzuzeigen. Wenn dieses Flag auf **true** gesetzt ist, haben die Eigenschaften [FontFormat](../get_fontformat/) und [ExportEmbeddedFonts](../get_exportembeddedfonts/) keine Wirkung, außerdem wird [ResourceSavingCallback](../get_resourcesavingcallback/) für Schriftarten nicht ausgelöst. Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts() const
```


## Beispiele



Zeigt, wie man Schriftarten nur vom Zielrechner verwendet, wenn man ein Dokument als HTML speichert.
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

## Siehe auch

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
