---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias 方法"
linktitle: "get_ImagesFolderAlias"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias 方法。指定用于构建写入 HTML 文档的图像 URI 的文件夹名称。默认在 C++ 中为空字符串。"
type: docs
weight: 39000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_imagesfolderalias/
---
## HtmlSaveOptions::get_ImagesFolderAlias method


指定用于构建写入 HTML 文档的图像 URI 的文件夹名称。默认是空字符串。

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias() const
```

## 备注


当您以 HTML 格式保存 [Document](../../../aspose.words/document/) 时，Aspose.Words 需要将文档中嵌入的所有图像保存为独立文件。[ImagesFolder](../get_imagesfolder/) 允许您指定图像的保存位置，而 [ImagesFolderAlias](./) 则允许指定图像 URI 的构建方式。

如果 [ImagesFolderAlias](./) 不是空字符串，则写入 HTML 的图像 URI 将为 *ImagesFolderAlias + <image file name>*。

如果 [ImagesFolderAlias](./) 是空字符串，则写入 HTML 的图像 URI 将为 *ImagesFolder + <image file name>*。

如果 [ImagesFolderAlias](./) 设置为 '.'（点），则无论其他选项如何，图像文件名都将以不带路径的形式写入 HTML。

指定用于构建图像 URI 的文件夹名称的另一种方式是使用 [ResourceFolderAlias](../get_resourcefolderalias/)。

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
