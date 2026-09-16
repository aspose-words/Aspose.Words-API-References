---
title: "Aspose::Words::Drawing::RelativeVerticalPosition 枚举"
linktitle: "RelativeVerticalPosition"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::RelativeVerticalPosition 枚举。指定形状或文本框的垂直位置相对于什么（在 C++ 中）。"
type: docs
weight: 34000
url: /zh/cpp/aspose.words.drawing/relativeverticalposition/
---
## RelativeVerticalPosition enum


指定形状或文本框的垂直位置相对于什么。

```cpp
enum class RelativeVerticalPosition
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 边距 | 0 | 指定垂直定位应相对于页面边距。 |
| Page | 1 | 对象相对于页面的顶部边缘进行定位。 |
| 段落 | 2 | 对象相对于包含锚点的段落顶部进行定位。 |
| 线 | 3 | 未记录。 |
| TopMargin | 4 | 指定垂直定位应相对于当前页面的顶部边距。 |
| BottomMargin | 5 | 指定垂直定位应相对于当前页面的底部边距。 |
| InsideMargin | 6 | 指定垂直定位应相对于当前页面的内侧边距。 |
| OutsideMargin | 7 | 指定垂直定位应相对于当前页面的外侧边距。 |
| TableDefault | n/a | 默认值是 [Margin](./)。 |
| TextFrameDefault | n/a | 默认值是 [Paragraph](./)。 |


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
