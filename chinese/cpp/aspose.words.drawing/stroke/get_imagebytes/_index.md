---
title: "Aspose::Words::Drawing::Stroke::get_ImageBytes 方法"
linktitle: "get_ImageBytes"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Stroke::get_ImageBytes 方法。定义笔画图像或图案填充的图像（在 C++ 中）。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.drawing/stroke/get_imagebytes/
---
## Stroke::get_ImageBytes method


定义用于描边图像或图案填充的图像。

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::Stroke::get_ImageBytes()
```


## 示例



展示如何处理形状描边特性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape stroke pattern border.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();

// 描边可以有两种颜色，这些颜色用于创建由双音调图像数据定义的图案。
// 单色描边不使用 Color2 属性。
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 128, 0, 0), stroke->get_Color());
ASPOSE_ASSERT_EQ(System::Drawing::Color::FromArgb(255, 255, 255, 0), stroke->get_Color2());

ASSERT_FALSE(System::TestTools::IsNull(stroke->get_ImageBytes()));
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"Drawing.StrokePattern.png", stroke->get_ImageBytes());
```

## 另见

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
