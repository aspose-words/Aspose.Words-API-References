---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder metod"
linktitle: "get_ImagesFolder"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder metod. Anger den fysiska mappen där bilder sparas när ett dokument exporteras till HTML‑format. Standardvärdet är en tom sträng i C++."
type: docs
weight: 38000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_imagesfolder/
---
## HtmlSaveOptions::get_ImagesFolder method


Anger den fysiska mappen där bilder sparas när ett dokument exporteras till HTML‑format. Standard är en tom sträng.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder() const
```

## Anmärkningar


När du sparar ett [Document](../../../aspose.words/document/) i HTML‑format måste Aspose.Words spara alla bilder som är inbäddade i dokumentet som separata filer. [ImagesFolder](./) låter dig ange var bilderna ska sparas och [ImagesFolderAlias](../get_imagesfolderalias/) låter dig ange hur bild‑URI:erna ska konstrueras.

Om du sparar ett dokument i en fil och anger ett filnamn sparar Aspose.Words som standard bilderna i samma mapp där dokumentfilen sparas. Använd [ImagesFolder](./) för att åsidosätta detta beteende.

Om du sparar ett dokument i en ström har Aspose.Words ingen mapp att spara bilderna i, men måste ändå spara dem någonstans. I så fall måste du ange en åtkomlig mapp i egenskapen [ImagesFolder](./) eller tillhandahålla anpassade strömmar via händelsehanteraren [ImageSavingCallback](../get_imagesavingcallback/).

Om mappen som anges av [ImagesFolder](./) inte finns kommer den att skapas automatiskt.

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where images should be saved.

## Exempel



Visar hur du anger mappen för lagring av länkade bilder efter att ha sparat till .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Ställ in ett alternativ för att exportera formulärfält som vanlig text istället för HTML‑inmatningselement.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## Se även

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
