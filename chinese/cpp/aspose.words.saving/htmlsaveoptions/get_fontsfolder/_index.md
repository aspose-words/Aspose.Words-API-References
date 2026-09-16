---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder 方法"
linktitle: "get_FontsFolder"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder 方法。指定在将文档导出为 HTML 时保存字体的物理文件夹。默认在 C++ 中为空字符串。"
type: docs
weight: 33000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolder/
---
## HtmlSaveOptions::get_FontsFolder method


指定将文档导出为 HTML 时保存字体的物理文件夹。默认值为空字符串。

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder() const
```

## 备注


当您以 HTML 格式保存 [Document](../../../aspose.words/document/) 且将 [ExportFontResources](../get_exportfontresources/) 设置为 **true** 时，Aspose.Words 需要将文档中使用的字体保存为独立文件。[FontsFolder](./) 允许您指定字体保存的位置，而 [FontsFolderAlias](../get_fontsfolderalias/) 则允许指定字体 URI 的构建方式。

如果您将文档保存到文件并提供文件名，Aspose.Words 默认会将字体保存在与文档文件相同的文件夹中。使用 [FontsFolder](./) 可覆盖此行为。

如果您将文档保存到流中，Aspose.Words 没有用于保存字体的文件夹，但仍需要将字体保存到某处。在这种情况下，您需要在 [FontsFolder](./) 属性中指定一个可访问的文件夹，或通过 [FontSavingCallback](../get_fontsavingcallback/) 事件处理程序提供自定义流。

如果 [FontsFolder](./) 指定的文件夹不存在，它将自动创建。

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where fonts should be saved.

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
