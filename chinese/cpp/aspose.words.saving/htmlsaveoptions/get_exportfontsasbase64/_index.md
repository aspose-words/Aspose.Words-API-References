---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64 方法"
linktitle: "get_ExportFontsAsBase64"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64 方法。指定是否应以 Base64 编码将字体资源嵌入到 HTML 中。默认在 C++ 中为 false。"
type: docs
weight: 17000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_exportfontsasbase64/
---
## HtmlSaveOptions::get_ExportFontsAsBase64 method


指定是否应以 Base64 编码将字体资源嵌入到 HTML 中。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64() const
```

## 备注


默认情况下，字体会写入单独的文件。如果此选项设置为 **true**，字体将以 Base64 编码嵌入文档的 CSS 中。

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
