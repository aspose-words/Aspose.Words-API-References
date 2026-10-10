---
title: "Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape 方法"
linktitle: "get_CurrentShape"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape 方法。获取即将在 C++ 中保存的形状或组形状对应的 ShapeBase 对象。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.saving/imagesavingargs/get_currentshape/
---
## ImageSavingArgs::get_CurrentShape method


获取即将保存的形状或组形状对应的 [ShapeBase](../../../aspose.words.drawing/shapebase/) 对象。

```cpp
System::SharedPtr<Aspose::Words::Drawing::ShapeBase> Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape() const
```

## 备注


[IImageSavingCallback](../../iimagesavingcallback/) can be fired while saving either a shape or a group shape. That's why the property has [ShapeBase](../../../aspose.words.drawing/shapebase/) type. You can check whether it's a group shape comparing [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) with [Group](../../../aspose.words.drawing/shapetype/) or by casting it to one of derived classes: [Shape](../../../aspose.words.drawing/shape/) or [GroupShape](../../../aspose.words.drawing/groupshape/).

Aspose.Words 使用文档文件名和唯一编号为文档中找到的每个图像生成唯一的文件名。您可以使用 [CurrentShape](./) 属性，通过检查形状属性（如仅适用于 Shape 的 [Title](../../../aspose.words.drawing/imagedata/get_title/)、仅适用于 Shape 的 [SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) 和 [Name](../../../aspose.words.drawing/shapebase/get_name/)）来生成一个 \"better\" 文件名。当然，您可以使用任何其他属性或标准来构建文件名，但请注意，子文件名在导出操作中必须是唯一的。

文档中的某些图像可能不可用。要检查图像可用性，请使用 [IsImageAvailable](../get_isimageavailable/) 属性。
## 另见

* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
