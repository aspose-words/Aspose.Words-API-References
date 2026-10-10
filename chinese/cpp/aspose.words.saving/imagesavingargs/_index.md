---
title: "Aspose::Words::Saving::ImageSavingArgs 类"
linktitle: "ImageSavingArgs"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImageSavingArgs 类。提供 ImageSaving() 事件的数据。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class


提供 [ImageSaving()](../iimagesavingcallback/imagesaving/) 事件的数据。要了解更多信息，请访问 [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) 文档文章。

```cpp
class ImageSavingArgs : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_CurrentShape](./get_currentshape/)() const | 获取对应于即将保存的形状或组形状的 [ShapeBase](../../aspose.words.drawing/shapebase/) 对象。 |
| [get_Document](./get_document/)() | 获取当前正在保存的文档对象。 |
| [get_ImageFileName](./get_imagefilename/)() const | 获取或设置图像将要保存的文件名（不含路径）。 |
| [get_ImageStream](./get_imagestream/)() const | 允许指定图像将要保存的流。 |
| [get_IsImageAvailable](./get_isimageavailable/)() const | 如果当前图像可导出，则返回 **true**。 |
| [get_KeepImageStreamOpen](./get_keepimagestreamopen/)() const | 指定 Aspose.Words 在保存图像后是保持流打开还是关闭它。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName](./get_imagefilename/) 的 setter。 |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | 用于设置 [Aspose::Words::Saving::ImageSavingArgs::get_ImageStream](./get_imagestream/) 的 setter。 |
| [set_ImageStream](./set_imagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepImageStreamOpen](./set_keepimagestreamopen/)(bool) | 用于设置 [Aspose::Words::Saving::ImageSavingArgs::get_KeepImageStreamOpen](./get_keepimagestreamopen/) 的 setter。 |
| static [Type](./type/)() |  |
## 备注


默认情况下，当 Aspose.Words 将文档保存为 HTML 时，它会将每个图像保存到单独的文件中。Aspose.Words 使用文档文件名和唯一编号为文档中找到的每个图像生成唯一的文件名。

[ImageSavingArgs](./) allows to redefine how image file names are generated or to completely circumvent saving of images into files by providing your own stream objects.

要应用您自己的图像文件名生成逻辑，请使用 [ImageFileName](./get_imagefilename/)、[CurrentShape](./get_currentshape/) 和 [IsImageAvailable](./get_isimageavailable/) 属性。

要将图像保存到流而不是文件，请使用 [ImageStream](./get_imagestream/) 属性。
## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
