---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages 方法"
linktitle: "get_ExportOriginalUrlForLinkedImages"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages 方法。指定是否应使用原始 URL 作为链接图像的 URL。默认值在 C++ 中为 false。"
type: docs
weight: 22000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages method


指定是否应使用原始 URL 作为链接图像的 URL。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages() const
```

## 备注


如果将值设置为 **true**[SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) ，该值将用作链接图像的 URL，且链接图像不会加载到文档的文件夹或 [ImagesFolder](../get_imagesfolder/) 中。

如果将值设置为 **false**，链接图像将加载到文档的文件夹或 [ImagesFolder](../get_imagesfolder/) 中，并且每个链接图像的 URL 将根据文档的文件夹、[ImagesFolder](../get_imagesfolder/) 和 [ImagesFolderAlias](../get_imagesfolderalias/) 属性构建。

## 示例



展示如何为 Aspose.Words 在保存文档为 HTML 时创建的外部保存资源设置文件夹和文件夹别名。
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

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
