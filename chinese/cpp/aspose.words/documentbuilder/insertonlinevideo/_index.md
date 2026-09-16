---
title: "Aspose::Words::DocumentBuilder::InsertOnlineVideo 方法"
linktitle: "InsertOnlineVideo"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertOnlineVideo 方法。在 C++ 中将在线视频对象插入文档并按指定尺寸缩放。"
type: docs
weight: 43000
url: /zh/cpp/aspose.words/documentbuilder/insertonlinevideo/
---
## DocumentBuilder::InsertOnlineVideo(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


将在线视频对象插入文档并按指定大小缩放。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| videoUrl | const System::String\& | 视频的 URL。 |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | 指定测量图像距离的起点位置。 |
| left | double | 从原点到图像左侧的距离（点）。 |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | 指定测量图像距离的起点位置。 |
| top | double | 从原点到图像顶部的距离（点）。 |
| width | double | 图像的宽度（以点为单位）。可以是负值或零，以请求 100% 缩放。 |
| height | double | 图像的高度（以点为单位）。可以是负值或零，以请求 100% 缩放。 |
| wrapType | Aspose::Words::Drawing::WrapType | 指定文本环绕图像的方式。 |

### ReturnValue

刚刚插入的图像节点。
## 备注


您可以使用此方法返回的 [Shape](../../../aspose.words.drawing/shape/) 对象更改图像大小、位置、定位方式以及其他设置。

支持从以下资源插入在线视频：

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



如果您的在线视频未正确显示，请使用 [InsertOnlineVideo()](../)，它接受自定义嵌入的 HTML 代码。

嵌入视频的代码因提供商而异，请查阅您所选的相应提供商以获取详细信息。

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


将在线视频对象插入文档并按指定大小缩放。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| videoUrl | const System::String\& | 视频的 URL。 |
| videoEmbedCode | const System::String\& | 视频的嵌入代码。 |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | 缩略图图像的字节。 |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | 指定测量图像距离的起点位置。 |
| left | double | 从原点到图像左侧的距离（点）。 |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | 指定测量图像距离的起点位置。 |
| top | double | 从原点到图像顶部的距离（点）。 |
| width | double | 图像的宽度（以点为单位）。可以是负值或零，以请求 100% 缩放。 |
| height | double | 图像的高度（以点为单位）。可以是负值或零，以请求 100% 缩放。 |
| wrapType | Aspose::Words::Drawing::WrapType | 指定文本环绕图像的方式。 |

### ReturnValue

刚刚插入的图像节点。
## 备注


您可以使用此方法返回的 [Shape](../../../aspose.words.drawing/shape/) 对象更改图像大小、位置、定位方式以及其他设置。

## 示例



展示如何使用自定义缩略图将在线视频插入文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String videoUrl = u"https://vimeo.com/52477838";
System::String videoEmbedCode = System::String(u"<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" ") + u"title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

System::ArrayPtr<uint8_t> thumbnailImageBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(thumbnailImageBytes);
    {
        System::SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromStream(stream);
        // 下面提供了两种创建带有自定义缩略图的形状的方法，该缩略图链接到在线视频
        // 在 Microsoft Word 中单击该形状时将播放视频。
        // 1 - 在构建器的节点插入光标处插入内联形状：
        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image->get_Width(), image->get_Height());

        builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

        // 2 - 插入浮动形状：
        double left = builder->get_PageSetup()->get_RightMargin() - image->get_Width();
        double top = builder->get_PageSetup()->get_BottomMargin() - image->get_Height();

        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, left, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, top, image->get_Width(), image->get_Height(), Aspose::Words::Drawing::WrapType::Square);
    }
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) method


将在线视频对象插入文档并按指定大小缩放。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, double width, double height)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| videoUrl | const System::String\& | 视频的 URL。 |
| videoEmbedCode | const System::String\& | 视频的嵌入代码。 |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | 缩略图图像的字节。 |
| width | double | 图像的宽度（以点为单位）。可以是负值或零，以请求 100% 缩放。 |
| height | double | 图像的高度（以点为单位）。可以是负值或零，以请求 100% 缩放。 |

### ReturnValue

刚刚插入的图像节点。
## 备注


您可以使用此方法返回的 [Shape](../../../aspose.words.drawing/shape/) 对象更改图像大小、位置、定位方式以及其他设置。

## 示例



展示如何使用自定义缩略图将在线视频插入文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String videoUrl = u"https://vimeo.com/52477838";
System::String videoEmbedCode = System::String(u"<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" ") + u"title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

System::ArrayPtr<uint8_t> thumbnailImageBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(thumbnailImageBytes);
    {
        System::SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromStream(stream);
        // 下面提供了两种创建带有自定义缩略图的形状的方法，该缩略图链接到在线视频
        // 在 Microsoft Word 中单击该形状时将播放视频。
        // 1 - 在构建器的节点插入光标处插入内联形状：
        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image->get_Width(), image->get_Height());

        builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

        // 2 - 插入浮动形状：
        double left = builder->get_PageSetup()->get_RightMargin() - image->get_Width();
        double top = builder->get_PageSetup()->get_BottomMargin() - image->get_Height();

        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, left, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, top, image->get_Width(), image->get_Height(), Aspose::Words::Drawing::WrapType::Square);
    }
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, double, double) method


将在线视频对象插入文档并按指定大小缩放。

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, double width, double height)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| videoUrl | const System::String\& | 视频的 URL。 |
| width | double | 图像的宽度（以点为单位）。可以是负值或零，以请求 100% 缩放。 |
| height | double | 图像的高度（以点为单位）。可以是负值或零，以请求 100% 缩放。 |

### ReturnValue

刚刚插入的图像节点。
## 备注


您可以使用此方法返回的 [Shape](../../../aspose.words.drawing/shape/) 对象更改图像大小、位置、定位方式以及其他设置。

支持从以下资源插入在线视频：

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



如果您的在线视频未正确显示，请使用 [InsertOnlineVideo()](../)，它接受自定义嵌入的 HTML 代码。

嵌入视频的代码因提供商而异，请查阅您所选的相应提供商以获取详细信息。

## 示例



展示如何使用 URL 将在线视频插入文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertOnlineVideo(u"https://youtu.be/g1N9ke8Prmk", 360, 270);

// 我们可以通过单击形状在 Microsoft Word 中观看视频。
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertVideoWithUrl.docx");
```

## 另见

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
