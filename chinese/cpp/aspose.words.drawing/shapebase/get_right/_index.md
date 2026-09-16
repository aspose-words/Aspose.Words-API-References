---
title: "Aspose::Words::Drawing::ShapeBase::get_Right 方法"
linktitle: "get_Right"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_Right 方法。获取形状所在包含块右边缘的位置（C++）。"
type: docs
weight: 44000
url: /zh/cpp/aspose.words.drawing/shapebase/get_right/
---
## ShapeBase::get_Right method


获取形状所在包含块的右边缘位置。

```cpp
double Aspose::Words::Drawing::ShapeBase::get_Right()
```

## 备注


对于顶层形状，该值以点为单位，并相对于形状锚点。

对于组内的形状，该值使用父组的坐标空间和单位。

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

## 另见

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
