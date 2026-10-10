---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder metod"
linktitle: "get_FontsFolder"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder metod. Anger den fysiska mappen där teckensnitt sparas när ett dokument exporteras till HTML. Standard är en tom sträng i C++."
type: docs
weight: 33000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolder/
---
## HtmlSaveOptions::get_FontsFolder method


Anger den fysiska mappen där teckensnitt sparas när ett dokument exporteras till HTML. Standard är en tom sträng.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder() const
```

## Anmärkningar


När du sparar ett [Document](../../../aspose.words/document/) i HTML-format och [ExportFontResources](../get_exportfontresources/) är satt till **true**, måste Aspose.Words spara teckensnitt som används i dokumentet som fristående filer. [FontsFolder](./) låter dig ange var teckensnitten ska sparas och [FontsFolderAlias](../get_fontsfolderalias/) låter dig ange hur teckensnitts-URI:erna ska konstrueras.

Om du sparar ett dokument i en fil och anger ett filnamn, sparar Aspose.Words som standard teckensnitten i samma mapp där dokumentfilen sparas. Använd [FontsFolder](./) för att åsidosätta detta beteende.

Om du sparar ett dokument i en ström har Aspose.Words ingen mapp att spara teckensnitten i, men måste ändå spara teckensnitten någonstans. I så fall måste du ange en åtkomlig mapp i egenskapen [FontsFolder](./) eller tillhandahålla anpassade strömmar via händelsehanteraren [FontSavingCallback](../get_fontsavingcallback/).

Om mappen som anges av [FontsFolder](./) inte finns, kommer den att skapas automatiskt.

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where fonts should be saved.

## Exempel



Visar hur man ställer in mappar och mapparalias för externa resurser som Aspose.Words kommer att skapa när ett dokument sparas som HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
options->set_ExportFontResources(true);
options->set_ImageResolution(72);
options->set_FontResourcesSubsettingSizeThreshold(0);
options->set_FontsFolder(get_ArtifactsDir() + u"Fonts");
options->set_ImagesFolder(get_ArtifactsDir() + u"Images");
options->set_ResourceFolder(get_ArtifactsDir() + u"Resources");
options->set_FontsFolderAlias(u"http://example.com/fonts");
options->set_ImagesFolderAlias(u"http://example.com/images");
options->set_ResourceFolderAlias(u"http://example.com/resources");
options->set_ExportOriginalUrlForLinkedImages(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.FolderAlias.html", options);
```

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
