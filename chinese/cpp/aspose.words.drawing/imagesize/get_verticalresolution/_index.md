---
title: "Aspose::Words::Drawing::ImageSize::get_VerticalResolution 方法"
linktitle: "get_VerticalResolution"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ImageSize::get_VerticalResolution 方法。获取 C++ 中的垂直分辨率（DPI）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.drawing/imagesize/get_verticalresolution/
---
## ImageSize::get_VerticalResolution method


获取垂直分辨率（DPI）。

```cpp
double Aspose::Words::Drawing::ImageSize::get_VerticalResolution() const
```


## 示例



展示如何读取形状中图像的属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 在文档中插入一个包含来自本地文件系统的图像的形状。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// 如果形状包含图像，其 ImageData 属性将有效，
// 并且它将包含一个 ImageSize 对象。
System::SharedPtr<Aspose::Words::Drawing::ImageSize> imageSize = shape->get_ImageData()->get_ImageSize();

// ImageSize 对象包含关于形状内图像的只读信息。
ASSERT_EQ(400, imageSize->get_HeightPixels());
ASSERT_EQ(400, imageSize->get_WidthPixels());

const double delta = 0.05;
ASSERT_NEAR(95.98, imageSize->get_HorizontalResolution(), delta);
ASSERT_NEAR(95.98, imageSize->get_VerticalResolution(), delta);

// 我们可以根据图像的尺寸来确定形状的大小，以避免拉伸图像。
shape->set_Width(imageSize->get_WidthPoints() * 2);
shape->set_Height(imageSize->get_HeightPoints() * 2);

doc->Save(get_ArtifactsDir() + u"Drawing.ImageSize.docx");
```

## 另见

* Class [ImageSize](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
