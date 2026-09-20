---
title: "Aspose::Words::Drawing::WrapType enum"
linktitle: "WrapType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::WrapType 枚举。指定文本在 C++ 中如何环绕形状或图片。"
type: docs
weight: 45000
url: /zh/cpp/aspose.words.drawing/wraptype/
---
## WrapType enum


指定文本环绕形状或图片的方式。

```cpp
enum class WrapType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 3 | 形状周围没有文本换行。该形状位于文本的后面或前面。 |
| Inline | 0 | 形状保持在与文本相同的层，并被视为字符。 |
| TopBottom | 1 | 文本在形状顶部停止，并在形状下方的行重新开始。 |
| Square | 2 | 在形状的方形边界框的所有侧面环绕文本。 |
| Tight | 4 | 紧贴形状的边缘进行包裹，而不是围绕边界框进行包裹。 |
| 通过 | 5 | 与 Tight 相同，但在形状的任何开放部分内部进行包裹。 |


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
