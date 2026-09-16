---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias 方法"
linktitle: "get_FontsFolderAlias"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias 方法。指定用于构建写入 HTML 文档的字体 URI 的文件夹名称。默认在 C++ 中为空字符串。"
type: docs
weight: 34000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolderalias/
---
## HtmlSaveOptions::get_FontsFolderAlias method


指定用于构建写入 HTML 文档的字体 URI 的文件夹名称。默认值为空字符串。

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias() const
```

## 备注


当您以 HTML 格式保存 [Document](../../../aspose.words/document/) 且将 [ExportFontResources](../get_exportfontresources/) 设置为 **true** 时，Aspose.Words 需要将文档中使用的字体保存为独立文件。[FontsFolder](../get_fontsfolder/) 允许您指定字体保存的位置，而 [FontsFolderAlias](./) 则允许指定字体 URI 的构建方式。

如果 [FontsFolderAlias](./) 不是空字符串，则写入 HTML 的字体 URI 将为 *FontsFolderAlias + <font file name>*。

如果 [FontsFolderAlias](./) 是空字符串，则写入 HTML 的字体 URI 将为 *FontsFolder + <font file name>*。

如果 [FontsFolderAlias](./) 被设置为 '.'（点），则无论其他选项如何，字体文件名都将以不带路径的形式写入 HTML。

指定用于构建字体 URI 的文件夹名称的另一种方法是使用 [ResourceFolderAlias](../get_resourcefolderalias/)。

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
