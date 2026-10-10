---
title: "Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing 方法"
linktitle: "get_UseAntiAliasing"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing 方法。获取或设置一个值，以确定在 C++ 中渲染时是否使用抗锯齿。"
type: docs
weight: 21000
url: /zh/cpp/aspose.words.saving/saveoptions/get_useantialiasing/
---
## SaveOptions::get_UseAntiAliasing method


获取或设置一个值，用于确定是否在渲染时使用抗锯齿。

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing() const
```

## 备注


默认值为 **false**。当此值设置为 **true** 时，渲染将使用抗锯齿。

当文档导出为以下格式时使用此属性：[Tiff](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Jpeg](../../../aspose.words/saveformat/), [Emf](../../../aspose.words/saveformat/)。当文档导出为 [Html](../../../aspose.words/saveformat/), [Mhtml](../../../aspose.words/saveformat/), [Epub](../../../aspose.words/saveformat/), [Azw3](../../../aspose.words/saveformat/) 或 [Mobi](../../../aspose.words/saveformat/) 格式时，此选项用于栅格图像。

## 示例



展示如何使用 [SaveOptions](../) 提高渲染文档的质量。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(60);
builder->Writeln(u"Some text.");

System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.Default.jpg", options);

options->set_UseAntiAliasing(true);
options->set_UseHighQualityRendering(true);

doc->Save(get_ArtifactsDir() + u"Document.ImageSaveOptions.HighQuality.jpg", options);
```

## 另见

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
