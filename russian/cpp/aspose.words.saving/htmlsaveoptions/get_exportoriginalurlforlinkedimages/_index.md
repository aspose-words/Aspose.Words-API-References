---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages метод"
linktitle: "get_ExportOriginalUrlForLinkedImages"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages метод. Указывает, следует ли использовать оригинальный URL в качестве URL связанных изображений. Значение по умолчанию — false в C++."
type: docs
weight: 22000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages method


Указывает, следует ли использовать оригинальный URL в качестве URL связанных изображений. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages() const
```

## Примечания


Если значение установлено в **true**[SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) значение используется как URL связанных изображений, и связанные изображения не загружаются в папку документа или [ImagesFolder](../get_imagesfolder/).

Если значение установлено в **false**, связанные изображения загружаются в папку документа или [ImagesFolder](../get_imagesfolder/), и URL каждого связанного изображения формируется в зависимости от папки документа, свойств [ImagesFolder](../get_imagesfolder/) и [ImagesFolderAlias](../get_imagesfolderalias/).

## Примеры



Показывает, как задавать папки и псевдонимы папок для внешних сохраняемых ресурсов, которые Aspose.Words создаст при сохранении документа в HTML.
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

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
