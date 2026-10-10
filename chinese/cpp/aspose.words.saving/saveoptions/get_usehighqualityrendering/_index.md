---
title: "Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering 方法"
linktitle: "get_UseHighQualityRendering"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering 方法。获取或设置一个值，以决定是否在 C++ 中使用高质量（即慢速）渲染算法。"
type: docs
weight: 22000
url: /zh/cpp/aspose.words.saving/saveoptions/get_usehighqualityrendering/
---
## SaveOptions::get_UseHighQualityRendering method


获取或设置一个值，用于确定是否使用高质量（即慢速）的渲染算法。

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering() const
```

## 备注


默认值为 **false**。

当文档导出为图像格式时使用此属性：[Tiff](../../../aspose.words/saveformat/)、[Png](../../../aspose.words/saveformat/)、[Bmp](../../../aspose.words/saveformat/)、[Jpeg](../../../aspose.words/saveformat/)、[Emf](../../../aspose.words/saveformat/)。

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
