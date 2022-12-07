---
title: get_ImagesFolderAlias
second_title: Aspose.Words for C++ API Reference
description: Specifies the name of the folder used to construct image URIs written into an HTML document. Default is an empty string.
type: docs
weight: 495
url: /cpp/aspose.words.saving/htmlsaveoptions/get_imagesfolderalias/
---
## HtmlSaveOptions::get_ImagesFolderAlias method


Specifies the name of the folder used to construct image URIs written into an HTML document. Default is an empty string.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias() const
```

## Remarks


When you save a [Document](../../../aspose.words/document/) in HTML format, Aspose.Words needs to save all images embedded in the document as standalone files. [ImagesFolder](../get_imagesfolder/) allows you to specify where the images will be saved and [ImagesFolderAlias](./) allows to specify how the image URIs will be constructed.

If [ImagesFolderAlias](./) is not an empty string, then the image URI written to HTML will be *ImagesFolderAlias + <image file name>*.

If [ImagesFolderAlias](./) is an empty string, then the image URI written to HTML will be *ImagesFolder + <image file name>*.

If [ImagesFolderAlias](./) is set to '.' (dot), then the image file name will be written to HTML without path regardless of other options.

Alternative way to specify the name of the folder to construct image URIs is to use [ResourceFolderAlias](../get_resourcefolderalias/).

## Examples



Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

auto options = MakeObject<HtmlSaveOptions>();
options->set_CssStyleSheetType(CssStyleSheetType::External);
options->set_ExportFontResources(true);
options->set_ImageResolution(72);
options->set_FontResourcesSubsettingSizeThreshold(0);
options->set_FontsFolder(ArtifactsDir + u"Fonts");
options->set_ImagesFolder(ArtifactsDir + u"Images");
options->set_ResourceFolder(ArtifactsDir + u"Resources");
options->set_FontsFolderAlias(u"http://example.com/fonts");
options->set_ImagesFolderAlias(u"http://example.com/images");
options->set_ResourceFolderAlias(u"http://example.com/resources");
options->set_ExportOriginalUrlForLinkedImages(true);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.FolderAlias.html", options);
```

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
