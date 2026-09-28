---
title: "метод Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts"
linktitle: "get_UseTargetMachineFonts"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts. Флаг указывает, должны ли шрифты с целевой машины использоваться для отображения документа. Если этот флаг установлен в true, свойства FontFormat и ExportEmbeddedFonts не действуют, также ResourceSavingCallback не вызывается для шрифтов. По умолчанию false в C++."
type: docs
weight: 20000
url: /ru/cpp/aspose.words.saving/htmlfixedsaveoptions/get_usetargetmachinefonts/
---
## HtmlFixedSaveOptions::get_UseTargetMachineFonts method


Флаг указывает, должны ли шрифты с целевой машины использоваться для отображения документа. Если этот флаг установлен в **true**, свойства [FontFormat](../get_fontformat/) и [ExportEmbeddedFonts](../get_exportembeddedfonts/) не действуют, также [ResourceSavingCallback](../get_resourcesavingcallback/) не вызывается для шрифтов. По умолчанию **false**.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts() const
```


## Примеры



Показывает, как использовать шрифты только с целевой машины при сохранении документа в HTML.
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

## См. также

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
