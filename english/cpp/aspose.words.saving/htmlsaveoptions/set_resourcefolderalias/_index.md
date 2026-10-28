---
title: Aspose::Words::Saving::HtmlSaveOptions::set_ResourceFolderAlias method
linktitle: set_ResourceFolderAlias
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::set_ResourceFolderAlias method. Specifies the name of the folder used to construct URIs of all resources written into an HTML document. Default is an empty string in C++.'
type: docs
weight: 91000
url: /cpp/aspose.words.saving/htmlsaveoptions/set_resourcefolderalias/
---
## HtmlSaveOptions::set_ResourceFolderAlias method


Specifies the name of the folder used to construct URIs of all resources written into an HTML document. Default is an empty string.

```cpp
void Aspose::Words::Saving::HtmlSaveOptions::set_ResourceFolderAlias(const System::String & value)
```

## Remarks


[ResourceFolderAlias](../get_resourcefolderalias/) is the simplest way to specify how URIs for all resource files should be constructed. Same information can be specified for images and fonts separately via [ImagesFolderAlias](../get_imagesfolderalias/) and [FontsFolderAlias](../get_fontsfolderalias/) properties, respectively. However, there is no individual property for CSS. 

[ResourceFolderAlias](../get_resourcefolderalias/) has lower priority than [FontsFolderAlias](../get_fontsfolderalias/) and [ImagesFolderAlias](../get_imagesfolderalias/). For example, if both [ResourceFolderAlias](../get_resourcefolderalias/) and [FontsFolderAlias](../get_fontsfolderalias/) are specified, fonts' URIs will be constructed using [FontsFolderAlias](../get_fontsfolderalias/), while URIs of images and CSS will be constructed using [ResourceFolderAlias](../get_resourcefolderalias/).

If [ResourceFolderAlias](../get_resourcefolderalias/) is empty, the [ResourceFolder](../get_resourcefolder/) property value will be used to construct resource URIs.

If [ResourceFolderAlias](../get_resourcefolderalias/) is set to '.' (dot), resource URIs will contain file names only, without any path.
## Examples


Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Rendering.docx"));

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_CssStyleSheetType(CssStyleSheetType::External);
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
## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
