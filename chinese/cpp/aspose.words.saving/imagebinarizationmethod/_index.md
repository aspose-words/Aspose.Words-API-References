---
title: "Aspose::Words::Saving::ImageBinarizationMethod 枚举"
linktitle: "ImageBinarizationMethod"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImageBinarizationMethod 枚举。指定在 C++ 中用于二值化图像的方法。"
type: docs
weight: 63000
url: /zh/cpp/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enum


指定用于二值化图像的方法。

```cpp
enum class ImageBinarizationMethod
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Threshold | 0 | 指定阈值方法。 |
| FloydSteinbergDithering | 1 | 指定使用 Floyd‑Steinberg 误差扩散方法进行抖动。 |


## 示例



展示如何在使用 Floyd‑Steinberg 方法渲染 TIFF 图像时设置 TIFF 二值化误差阈值。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// 当我们将文档保存为 TIFF 时，可以传递一个 SaveOptions 对象来
// 调整 Aspose.Words 在渲染此图像时应用的抖动。
// "ThresholdForFloydSteinbergDithering" 属性的默认值为 128。
// 较高的数值往往会产生更暗的图像。
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);
options->set_TiffCompression(Aspose::Words::Saving::TiffCompression::Ccitt3);
options->set_TiffBinarizationMethod(Aspose::Words::Saving::ImageBinarizationMethod::FloydSteinbergDithering);
options->set_ThresholdForFloydSteinbergDithering(240);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
