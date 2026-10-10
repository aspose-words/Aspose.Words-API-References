---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias Methode"
linktitle: "get_ResourceFolderAlias"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias Methode. Gibt den Namen des Ordners an, der zum Erstellen von URIs aller Ressourcen verwendet wird, die in ein HTML-Dokument geschrieben werden. Standard ist ein leerer String in C++."
type: docs
weight: 44000
url: /de/cpp/aspose.words.saving/htmlsaveoptions/get_resourcefolderalias/
---
## HtmlSaveOptions::get_ResourceFolderAlias method


Gibt den Namen des Ordners an, der zum Erstellen von URIs aller in ein HTML‑Dokument geschriebenen Ressourcen verwendet wird. Standard ist ein leerer String.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias() const
```

## Hinweise


[ResourceFolderAlias](./) is the simplest way to specify how URIs for all resource files should be constructed. Same information can be specified for images and fonts separately via [ImagesFolderAlias](../get_imagesfolderalias/) and [FontsFolderAlias](../get_fontsfolderalias/) properties, respectively. However, there is no individual property for CSS.

[ResourceFolderAlias](./) has lower priority than [FontsFolderAlias](../get_fontsfolderalias/) and [ImagesFolderAlias](../get_imagesfolderalias/). For example, if both [ResourceFolderAlias](./) and [FontsFolderAlias](../get_fontsfolderalias/) are specified, fonts' URIs will be constructed using [FontsFolderAlias](../get_fontsfolderalias/), while URIs of images and CSS will be constructed using [ResourceFolderAlias](./).

Wenn [ResourceFolderAlias](./) leer ist, wird der Wert der [ResourceFolder](../get_resourcefolder/) Eigenschaft zum Erstellen von Ressourcen-URIs verwendet.

Wenn [ResourceFolderAlias](./) auf '.' (Punkt) gesetzt ist, enthalten Ressourcen-URIs nur Dateinamen, ohne Pfad.

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
