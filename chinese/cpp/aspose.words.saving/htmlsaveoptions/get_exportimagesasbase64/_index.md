---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64 方法"
linktitle: "get_ExportImagesAsBase64"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64 方法。指定是否将图像以 Base64 格式保存到输出的 HTML、MHTML 或 EPUB 中。默认在 C++ 中为 false。"
type: docs
weight: 19000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_exportimagesasbase64/
---
## HtmlSaveOptions::get_ExportImagesAsBase64 method


指定是否以 Base64 格式将图像保存到输出的 HTML、MHTML 或 EPUB 中。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64() const
```

## 备注


当此属性设置为 **true** 时，图像数据会直接导出到 **img** 元素中，不会创建单独的文件。

## 示例



展示如何保存一个带有嵌入图像的 .html 文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportImagesAsBase64(exportImagesAsBase64);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportImagesAsBase64.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportImagesAsBase64.html");

ASSERT_TRUE(exportImagesAsBase64 ? outDocContents.Contains(u"<img src=\"data:image/png;base64") : outDocContents.Contains(u"<img src=\"HtmlSaveOptions.ExportImagesAsBase64.001.png\""));
```


展示如何在已保存的 HTML 文档中嵌入字体。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportFontsAsBase64(true);
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::Embedded);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportFontsAsBase64.html", options);
```

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
