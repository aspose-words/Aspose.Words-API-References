---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution Methode"
linktitle: "get_ImageResolution"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution Methode. Gibt die Ausgabebildauflösung für Bilder an, wenn in HTML, MHTML oder EPUB exportiert wird. Standard ist %96 dpi in C++."
type: docs
weight: 36000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_imageresolution/
---
## HtmlSaveOptions::get_ImageResolution method


Gibt die Ausgabeauflösung für Bilder beim Exportieren nach HTML, MHTML oder EPUB an. Standard ist **%96 dpi**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution() const
```

## Hinweise


Diese Eigenschaft wirkt sich auf Rasterbilder aus, wenn [ScaleImageToShapeSize](../get_scaleimagetoshapesize/) **true** ist und wirkt sich auf Metadateien aus, die als Rasterbilder exportiert werden. Einige Bildeigenschaften wie Zuschneiden oder Drehen erfordern das Speichern transformierter Bilder, und in diesem Fall werden transformierte Bilder in der angegebenen Auflösung erstellt.

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
