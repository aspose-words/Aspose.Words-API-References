---
title: "Aspose::Words::DocumentBuilder::get_CurrentSection 方法"
linktitle: "get_CurrentSection"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::get_CurrentSection 方法。获取在此 DocumentBuilder 中当前选中的章节（C++）。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words/documentbuilder/get_currentsection/
---
## DocumentBuilder::get_CurrentSection method


获取此 [DocumentBuilder](../) 中当前选中的章节。

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::DocumentBuilder::get_CurrentSection()
```


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

* Class [Section](../../section/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
