---
title: Aspose::Words::Saving::HtmlSaveOptions::set_FontsFolderAlias method
linktitle: set_FontsFolderAlias
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::set_FontsFolderAlias method. Specifies the name of the folder used to construct font URIs written into an HTML document. Default is an empty string in C++.'
type: docs
weight: 81000
url: /cpp/aspose.words.saving/htmlsaveoptions/set_fontsfolderalias/
---
## HtmlSaveOptions::set_FontsFolderAlias method


Specifies the name of the folder used to construct font URIs written into an HTML document. Default is an empty string.

```cpp
void Aspose::Words::Saving::HtmlSaveOptions::set_FontsFolderAlias(const System::String & value)
```

## Remarks


When you save a [Document](../../../aspose.words/document/) in HTML format and [ExportFontResources](../get_exportfontresources/) is set to **true**, Aspose.Words needs to save fonts used in the document as standalone files. [FontsFolder](../get_fontsfolder/) allows you to specify where the fonts will be saved and [FontsFolderAlias](../get_fontsfolderalias/) allows to specify how the font URIs will be constructed.

If [FontsFolderAlias](../get_fontsfolderalias/) is not an empty string, then the font URI written to HTML will be FontsFolderAlias + <font file name>.

If [FontsFolderAlias](../get_fontsfolderalias/) is an empty string, then the font URI written to HTML will be FontsFolder + <font file name>.

If [FontsFolderAlias](../get_fontsfolderalias/) is set to '.' (dot), then the font file name will be written to HTML without path regardless of other options.

Alternative way to specify the name of the folder to construct font URIs is to use [ResourceFolderAlias](../get_resourcefolderalias/).
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
