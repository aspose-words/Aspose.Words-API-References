---
title: "Aspose::Words::Drawing::ImageData::FitImageToShape 方法"
linktitle: "FitImageToShape"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ImageData::FitImageToShape 方法。将图像数据适配到 Shape 框架，使图像数据的宽高比与 Shape 框架的宽高比相匹配，适用于 C++。"
type: docs
weight: 1500
url: /zh/cpp/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData::FitImageToShape method


将图像数据适配到 [Shape](../../shape/) 框架，使图像数据的宽高比与 [Shape](../../shape/) 框架的宽高比相匹配。

```cpp
void Aspose::Words::Drawing::ImageData::FitImageToShape()
```


## 示例



展示如何将图像数据适配到 [Shape](../../shape/) 框架。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入图像形状并保持其方向为默认状态。
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 300, 450);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Barcode.png");
shape->get_ImageData()->FitImageToShape();

doc->Save(get_ArtifactsDir() + u"Shape.FitImageToShape.docx");
```

## 另见

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
