---
title: "Aspose::Words::ImageWatermarkOptions 类"
linktitle: "ImageWatermarkOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ImageWatermarkOptions 类。包含在使用图像添加水印时可以指定的选项。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 34000
url: /zh/cpp/aspose.words/imagewatermarkoptions/
---
## ImageWatermarkOptions class


包含在使用图像添加水印时可以指定的选项。要了解更多，请访问 [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/) 文档文章。

```cpp
class ImageWatermarkOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_IsWashout](./get_iswashout/)() const | 获取或设置一个布尔值，用于控制水印的淡化效果。默认值为 **true**。 |
| [get_Scale](./get_scale/)() const | 获取或设置以图像比例表示的缩放因子。默认值为 0 - 自动。 |
| [GetType](./gettype/)() const override |  |
| [ImageWatermarkOptions](./imagewatermarkoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsWashout](./set_iswashout/)(bool) | 用于设置 [Aspose::Words::ImageWatermarkOptions::get_IsWashout](./get_iswashout/) 的 setter。 |
| [set_Scale](./set_scale/)(double) | 用于设置 [Aspose::Words::ImageWatermarkOptions::get_Scale](./get_scale/) 的 setter。 |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
