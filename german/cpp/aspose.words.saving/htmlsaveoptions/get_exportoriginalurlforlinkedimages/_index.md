---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages Methode"
linktitle: "get_ExportOriginalUrlForLinkedImages"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages Methode. Gibt an, ob die ursprüngliche URL als URL der verknüpften Bilder verwendet werden soll. Der Standardwert ist false in C++."
type: docs
weight: 22000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages method


Gibt an, ob die ursprüngliche URL als URL der verknüpften Bilder verwendet werden soll. Standardwert ist **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages() const
```

## Hinweise


Wenn der Wert auf **true**[SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) gesetzt ist, wird der Wert als URL der verknüpften Bilder verwendet und die verknüpften Bilder werden nicht in den Ordner des Dokuments oder [ImagesFolder](../get_imagesfolder/) geladen.

Wenn der Wert auf **false** gesetzt ist, werden verknüpfte Bilder in den Ordner des Dokuments oder [ImagesFolder](../get_imagesfolder/) geladen und die URL jedes verknüpften Bildes wird abhängig vom Ordner des Dokuments, [ImagesFolder](../get_imagesfolder/) und den Eigenschaften von [ImagesFolderAlias](../get_imagesfolderalias/) erstellt.

## Beispiele



Zeigt, wie Ordner und Ordner‑Aliase für extern gespeicherte Ressourcen festgelegt werden, die Aspose.Words beim Speichern eines Dokuments nach HTML erstellt.
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

## Siehe auch

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
