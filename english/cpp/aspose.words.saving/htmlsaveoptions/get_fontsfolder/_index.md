---
title: get_FontsFolder
second_title: Aspose.Words for C++ API Reference
description: Specifies the physical folder where fonts are saved when exporting a document to HTML. Default is an empty string.
type: docs
weight: 404
url: /cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolder/
---
## HtmlSaveOptions.get_FontsFolder method


Specifies the physical folder where fonts are saved when exporting a document to HTML. Default is an empty string.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder() const
```


When you save a [Document](../../../aspose.words/document/) in HTML format and [ExportFontResources](../get_exportfontresources/) is set to **true**, Aspose.Words needs to save fonts used in the document as standalone files. [FontsFolder](./) allows you to specify where the fonts will be saved and [FontsFolderAlias](../get_fontsfolderalias/) allows to specify how the font URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the fonts in the same folder where the document file is saved. Use [FontsFolder](./) to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the fonts, but still needs to save the fonts somewhere. In this case, you need to specify an accessible folder in the [FontsFolder](./) property or provide custom streams via the [FontSavingCallback](../get_fontsavingcallback/) event handler.

If the folder specified by [FontsFolder](./) doesn't exist, it will be created automatically.

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where fonts should be saved.

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

