---
title: "Aspose::Words::Drawing::ShapeBase::get_Width 方法"
linktitle: "get_Width"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_Width 方法。获取或设置形状所在容器块的宽度（C++）。"
type: docs
weight: 54000
url: /zh/cpp/aspose.words.drawing/shapebase/get_width/
---
## ShapeBase::get_Width method


获取或设置形状所在包含块的宽度。

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Width()
```

## 备注


对于顶层形状，值以点为单位。

对于组内的形状，该值使用父组的坐标空间和单位。

默认值为 0。

## 示例



展示如何插入浮动图像，并指定其位置和大小。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// 配置形状的 "RelativeHorizontalPosition" 属性，使其将 "Left" 属性的值视为
// 形状相对于页面左侧的水平距离，单位为点。
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);

// 将形状相对于页面左侧的水平距离设置为 100。
shape->set_Left(100);

// 以类似方式使用 "RelativeVerticalPosition" 属性，将形状定位在页面顶部以下 80pt 的位置。
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Top(80);

// 设置形状的高度，系统将自动按比例缩放宽度以保持尺寸。
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// "Bottom" 和 "Right" 属性包含图像的底部和右侧边缘。
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPositionSize.docx");
```


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

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
