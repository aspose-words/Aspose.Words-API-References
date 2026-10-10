---
title: "Aspose::Words::Drawing::ImageSize 类"
linktitle: "ImageSize"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ImageSize 类。包含有关图像大小和分辨率的信息。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.drawing/imagesize/
---
## ImageSize class


包含有关图像尺寸和分辨率的信息。要了解更多信息，请访问 [Working with Images](https://docs.aspose.com/words/cpp/working-with-images/) 文档文章。

```cpp
class ImageSize : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_HeightPixels](./get_heightpixels/)() const | 获取图像的像素高度。 |
| [get_HeightPoints](./get_heightpoints/)() | 获取图像的点高度。1 点等于 1/72 英寸。 |
| [get_HorizontalResolution](./get_horizontalresolution/)() const | 获取水平分辨率（DPI）。 |
| [get_VerticalResolution](./get_verticalresolution/)() const | 获取垂直分辨率（DPI）。 |
| [get_WidthPixels](./get_widthpixels/)() const | 获取图像的像素宽度。 |
| [get_WidthPoints](./get_widthpoints/)() | 获取图像的点宽度。1 点等于 1/72 英寸。 |
| [GetType](./gettype/)() const override |  |
| [ImageSize](./imagesize/)(int32_t, int32_t) | 将宽度和高度初始化为给定的像素值。将分辨率初始化为 96 DPI。 |
| [ImageSize](./imagesize/)(int32_t, int32_t, double, double) | 将宽度、高度和分辨率初始化为给定的值。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## 示例



展示如何使用图像调整形状大小。
```cpp
// 当我们使用 \"InsertImage\" 方法插入图像时，构建器会缩放显示图像的形状，使得，
// 当我们在 Microsoft Word 中以 100% 缩放查看文档时，形状以实际大小显示图像。
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// 400x400 的图像将创建一个 ImageData 对象，其图像大小为 300x300pt。
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// 如果形状的尺寸与图像数据的尺寸匹配，
// 则形状以原始大小显示图像。
ASPOSE_ASSERT_EQ(300.0, shape->get_Width());
ASPOSE_ASSERT_EQ(300.0, shape->get_Height());

// 将形状的整体大小缩小 50%。
System::WithLambda::setter_mul_wrap(GETTER_SETTER_LAMBDA_ARGS(shape, Width), 0.5);

// 缩放因子同时作用于宽度和高度，以保持形状的比例。
ASPOSE_ASSERT_EQ(150.0, shape->get_Width());
ASPOSE_ASSERT_EQ(150.0, shape->get_Height());

// 当我们调整形状大小时，图像数据的尺寸保持不变。
ASPOSE_ASSERT_EQ(300.0, imageSize->get_WidthPoints());
ASPOSE_ASSERT_EQ(300.0, imageSize->get_HeightPoints());

// 我们可以引用图像数据的尺寸，根据图像大小应用缩放。
shape->set_Width(imageSize->get_WidthPoints() * 1.1);

ASPOSE_ASSERT_EQ(330.0, shape->get_Width());
ASPOSE_ASSERT_EQ(330.0, shape->get_Height());

doc->Save(get_ArtifactsDir() + u"Image.ScaleImage.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
