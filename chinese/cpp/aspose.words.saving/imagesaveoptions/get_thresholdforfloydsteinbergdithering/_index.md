---
title: "Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering 方法"
linktitle: "get_ThresholdForFloydSteinbergDithering"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering 方法。获取或设置在 Floyd‑Steinberg 方法中决定二值化误差值的阈值。当 C++ 中的 ImageBinarizationMethod 为 FloydSteinbergDithering 时。"
type: docs
weight: 15000
url: /zh/cpp/aspose.words.saving/imagesaveoptions/get_thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions::get_ThresholdForFloydSteinbergDithering method


获取或设置在 Floyd‑Steinberg 方法中决定二值化误差值的阈值。当 [ImageBinarizationMethod](../../imagebinarizationmethod/) 为 [FloydSteinbergDithering](../../imagebinarizationmethod/) 时。

```cpp
uint8_t Aspose::Words::Saving::ImageSaveOptions::get_ThresholdForFloydSteinbergDithering() const
```

## 备注


默认值为 128。

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

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
