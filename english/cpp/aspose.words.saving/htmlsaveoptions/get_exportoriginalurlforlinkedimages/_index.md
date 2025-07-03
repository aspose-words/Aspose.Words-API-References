---
title: Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages method
linktitle: get_ExportOriginalUrlForLinkedImages
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages method. Specifies whether original URL should be used as the URL of the linked images. Default value is false in C++.'
type: docs
weight: 22000
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages method


Specifies whether original URL should be used as the URL of the linked images. Default value is **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages() const
```

## Remarks


If value is set to **true**[SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) value is used as the URL of linked images and linked images are not loaded into document's folder or [ImagesFolder](../get_imagesfolder/).

If value is set to **false** linked images are loaded into document's folder or [ImagesFolder](../get_imagesfolder/) and URL of each linked image is constructed depending on document's folder, [ImagesFolder](../get_imagesfolder/) and [ImagesFolderAlias](../get_imagesfolderalias/) properties.

## Examples



Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML. 
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

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
