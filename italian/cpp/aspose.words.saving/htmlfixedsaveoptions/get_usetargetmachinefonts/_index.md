---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts metodo"
linktitle: "get_UseTargetMachineFonts"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts metodo. Il flag indica se i caratteri dalla macchina di destinazione devono essere usati per visualizzare il documento. Se questo flag è impostato su true, le proprietà FontFormat e ExportEmbeddedFonts non hanno effetto, inoltre ResourceSavingCallback non viene eseguito per i caratteri. Il valore predefinito è false in C++."
type: docs
weight: 20000
url: /it/cpp/aspose.words.saving/htmlfixedsaveoptions/get_usetargetmachinefonts/
---
## HtmlFixedSaveOptions::get_UseTargetMachineFonts method


Il flag indica se i caratteri dalla macchina di destinazione devono essere usati per visualizzare il documento. Se questo flag è impostato su **true**, le proprietà [FontFormat](../get_fontformat/) e [ExportEmbeddedFonts](../get_exportembeddedfonts/) non hanno effetto, inoltre [ResourceSavingCallback](../get_resourcesavingcallback/) non viene eseguito per i caratteri. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts() const
```


## Esempi



Mostra come utilizzare solo i font dalla macchina di destinazione durante il salvataggio di un documento in HTML.
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

## Vedi anche

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
