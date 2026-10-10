---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder 方法"
linktitle: "get_ResourceFolder"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder 方法。指定在将文档导出为 HTML 时，所有资源（如图像、字体和外部 CSS）保存的物理文件夹。默认在 C++ 中为空字符串。"
type: docs
weight: 43000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_resourcefolder/
---
## HtmlSaveOptions::get_ResourceFolder method


指定将文档导出为 HTML 时，所有资源（如图像、字体和外部 CSS）保存的物理文件夹。默认是空字符串。

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder() const
```

## 备注


[ResourceFolder](./) is the simplest way to specify a folder where all resources should be written. Another way is to use individual properties [FontsFolder](../get_fontsfolder/), [ImagesFolder](../get_imagesfolder/), and [CssStyleSheetFileName](../get_cssstylesheetfilename/).

[ResourceFolder](./) has a lower priority than folders specified via [FontsFolder](../get_fontsfolder/), [ImagesFolder](../get_imagesfolder/), and [CssStyleSheetFileName](../get_cssstylesheetfilename/). For example, if both [ResourceFolder](./) and [FontsFolder](../get_fontsfolder/) are specified, fonts will be saved to [FontsFolder](../get_fontsfolder/), while images and CSS will be saved to [ResourceFolder](./).

如果 [ResourceFolder](./) 指定的文件夹不存在，将自动创建。

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
