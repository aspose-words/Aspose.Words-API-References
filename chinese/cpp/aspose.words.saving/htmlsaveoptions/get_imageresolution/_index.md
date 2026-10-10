---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution 方法"
linktitle: "get_ImageResolution"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution 方法。指定导出为 HTML、MHTML 或 EPUB 时图像的输出分辨率。默认在 C++ 中为 %96 dpi。"
type: docs
weight: 36000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_imageresolution/
---
## HtmlSaveOptions::get_ImageResolution method


指定导出为 HTML、MHTML 或 EPUB 时图像的输出分辨率。默认值为 **%96 dpi**。

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution() const
```

## 备注


当 [ScaleImageToShapeSize](../get_scaleimagetoshapesize/) 为 **true** 时，此属性会影响光栅图像，并影响导出为光栅图像的元文件。某些图像属性（如裁剪或旋转）需要保存已转换的图像，在这种情况下，已转换的图像会以给定的分辨率创建。

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
