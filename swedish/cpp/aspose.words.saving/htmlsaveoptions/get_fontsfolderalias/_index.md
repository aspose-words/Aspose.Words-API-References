---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias metod"
linktitle: "get_FontsFolderAlias"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias metod. Anger namnet på mappen som används för att konstruera teckensnitts-URI:er som skrivs in i ett HTML-dokument. Standard är en tom sträng i C++."
type: docs
weight: 34000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolderalias/
---
## HtmlSaveOptions::get_FontsFolderAlias method


Anger namnet på mappen som används för att konstruera teckensnitt-URI:er som skrivs in i ett HTML‑dokument. Standard är en tom sträng.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias() const
```

## Anmärkningar


När du sparar ett [Document](../../../aspose.words/document/) i HTML-format och [ExportFontResources](../get_exportfontresources/) är satt till **true**, måste Aspose.Words spara teckensnitt som används i dokumentet som fristående filer. [FontsFolder](../get_fontsfolder/) låter dig ange var teckensnitten ska sparas och [FontsFolderAlias](./) låter dig ange hur teckensnitts-URI:erna ska konstrueras.

Om [FontsFolderAlias](./) inte är en tom sträng, kommer teckensnitts-URI:n som skrivs till HTML att bli *FontsFolderAlias + <font file name>*.

Om [FontsFolderAlias](./) är en tom sträng, kommer teckensnitts-URI:n som skrivs till HTML att bli *FontsFolder + <font file name>*.

Om [FontsFolderAlias](./) är satt till '.' (punkt), kommer teckensnittsfilens namn att skrivas till HTML utan sökväg oavsett andra alternativ.

Ett alternativt sätt att ange mappens namn för att konstruera teckensnitts-URI:er är att använda [ResourceFolderAlias](../get_resourcefolderalias/).

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
