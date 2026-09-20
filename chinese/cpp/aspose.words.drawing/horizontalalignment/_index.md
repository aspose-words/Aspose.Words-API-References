---
title: "Aspose::Words::Drawing::HorizontalAlignment 枚举"
linktitle: "HorizontalAlignment"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::HorizontalAlignment 枚举。指定在 C++ 中浮动形状、文本框或浮动表格的水平对齐方式。"
type: docs
weight: 26000
url: /zh/cpp/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enum


指定浮动形状、文本框或浮动表格的水平对齐方式。

```cpp
enum class HorizontalAlignment
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 该对象被显式定位，通常使用其 **Left** 属性。 |
| Default | n/a | 同[None](./)。 |
| 左 | 1 | 指定对象应左对齐到水平对齐基准。 |
| 居中 | 2 | 指定对象应相对于水平对齐基准居中。 |
| 右 | 3 | 指定对象应右对齐到水平对齐基准。 |
| Inside | 4 | 指定对象应位于水平对齐基准的内部。 |
| Outside | 5 | 指定对象应位于水平对齐基准的外部。 |


## 示例



展示如何在页面中心插入浮动图像。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一个浮动图像，使其出现在重叠文本后面，并将其对齐到页面中心。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## 另见

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
