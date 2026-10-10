---
title: "Aspose::Words::Watermark::SetImage 方法"
linktitle: "SetImage"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Watermark::SetImage 方法。向文档中添加图像水印（C++）。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words/watermark/setimage/
---
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


向文档中添加图像水印。

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | 作为水印显示的图像。 |

## 示例



展示如何从本地文件系统中的图像创建水印。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 使用 ImageWatermarkOptions 对象修改图像水印的外观，
// 然后在从图像文件创建水印时传入该对象。
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// 我们有不同的选项来插入图像。
// 使用以下方法之一添加图像水印。
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## 另见

* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


向文档中添加图像水印。

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | 作为水印显示的图像。 |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | 定义图像水印的附加选项。 |

## 示例



展示如何从本地文件系统中的图像创建水印。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 使用 ImageWatermarkOptions 对象修改图像水印的外观，
// 然后在从图像文件创建水印时传入该对象。
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// 我们有不同的选项来插入图像。
// 使用以下方法之一添加图像水印。
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## 另见

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


向文档中添加图像水印。

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::IO::Stream> &imageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| imageStream | const System::SharedPtr\<System::IO::Stream\>\& | 包含显示为水印的图像数据的流。 |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | 定义图像水印的附加选项。 |

## 示例



展示如何从图像流创建水印。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 使用 ImageWatermarkOptions 对象修改图像水印的外观，
// 然后在从图像文件创建水印时传入该对象。
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);

{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open, System::IO::FileAccess::Read);
    doc->get_Watermark()->SetImage(imageStream, imageWatermarkOptions);
}

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermarkStream.docx");
```

## 另见

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


向文档中添加图像水印。

```cpp
void Aspose::Words::Watermark::SetImage(const System::String &imagePath, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| imagePath | const System::String\& | 显示为水印的图像文件的路径。 |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | 定义图像水印的附加选项。 |

## 示例



展示如何从本地文件系统中的图像创建水印。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 使用 ImageWatermarkOptions 对象修改图像水印的外观，
// 然后在从图像文件创建水印时传入该对象。
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// 我们有不同的选项来插入图像。
// 使用以下方法之一添加图像水印。
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## 另见

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
