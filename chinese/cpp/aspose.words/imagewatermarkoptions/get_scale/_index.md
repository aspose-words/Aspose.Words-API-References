---
title: "Aspose::Words::ImageWatermarkOptions::get_Scale 方法"
linktitle: "get_Scale"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ImageWatermarkOptions::get_Scale 方法。获取或设置以图像分数表示的比例因子。默认值为 0 - 自动，适用于 C++。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/imagewatermarkoptions/get_scale/
---
## ImageWatermarkOptions::get_Scale method


获取或设置以图像比例表示的缩放因子。默认值为 0 - 自动。

```cpp
double Aspose::Words::ImageWatermarkOptions::get_Scale() const
```

## 备注


有效值范围为 0 到 65.5（含）。

自动缩放表示水印将相对于页面边距按最大宽度和最大高度进行缩放。

## 示例



展示如何从本地文件系统中的图像创建水印。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 使用 ImageWatermarkOptions 对象修改图像水印的外观，
// 然后在从图像文件创建水印时传入该对象。
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// 我们有不同的选项来插入图像。
// 使用以下方法之一添加图像水印。
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## 另见

* Class [ImageWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
