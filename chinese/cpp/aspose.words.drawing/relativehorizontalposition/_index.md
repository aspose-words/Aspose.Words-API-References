---
title: "Aspose::Words::Drawing::RelativeHorizontalPosition enum"
linktitle: "RelativeHorizontalPosition"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::RelativeHorizontalPosition enum. 指定 C++ 中形状或文本框的水平位置相对于什么。"
type: docs
weight: 33000
url: /zh/cpp/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enum


指定形状或文本框的水平位置相对于什么。

```cpp
enum class RelativeHorizontalPosition
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 边距 | 0 | 指定水平定位应相对于页面边距。 |
| Page | 1 | 对象相对于页面的左边缘进行定位。 |
| 列 | 2 | 对象相对于列的左侧进行定位。 |
| 字符 | 3 | 对象相对于段落的左侧进行定位。 |
| LeftMargin | 4 | 指定水平定位应相对于页面的左边距。 |
| RightMargin | 5 | 指定水平定位应相对于页面的右边距。 |
| InsideMargin | 6 | 指定水平定位应相对于当前页面的内侧边距（奇数页为左边距，偶数页为右边距）。 |
| OutsideMargin | 7 | 指定水平定位应相对于当前页面的外侧边距（奇数页为右边距，偶数页为左边距）。 |
| Default | n/a | 默认值是 [Column](./)。 |


## 示例



展示如何插入图像并将其用作水印。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 将图像插入页眉，以便在每页上可见。
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);

// 将图像放置在页面中心。
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertWatermark.docx");
```


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
