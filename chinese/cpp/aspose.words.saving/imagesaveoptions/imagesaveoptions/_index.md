---
title: "Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions 构造函数"
linktitle: "ImageSaveOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions 构造函数。初始化此类的新实例，可用于在 C++ 中将渲染的图像保存为 Tiff、Png、Bmp、Jpeg、Emf、Eps、WebP 或 Svg 格式。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.saving/imagesaveoptions/imagesaveoptions/
---
## ImageSaveOptions::ImageSaveOptions constructor


初始化此类的新实例，可用于将渲染的图像保存为 [Tiff](../../../aspose.words/saveformat/)、[Png](../../../aspose.words/saveformat/)、[Bmp](../../../aspose.words/saveformat/)、[Jpeg](../../../aspose.words/saveformat/)、[Emf](../../../aspose.words/saveformat/)、[Eps](../../../aspose.words/saveformat/)、[WebP](../) 或 [Svg](../../../aspose.words/saveformat/) 格式。

```cpp
Aspose::Words::Saving::ImageSaveOptions::ImageSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | 可以是 [Tiff](../../../aspose.words/saveformat/)、[Png](../../../aspose.words/saveformat/)、[Bmp](../../../aspose.words/saveformat/)、[Jpeg](../../../aspose.words/saveformat/)、[Emf](../../../aspose.words/saveformat/)、[Eps](../../../aspose.words/saveformat/)[WebP](../) 或 [Svg](../../../aspose.words/saveformat/) 格式。 |

## 示例



展示如何在将文档保存为 JPEG 时配置压缩。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// 创建一个 "ImageSaveOptions" 对象，以便将其传递给文档的 "Save" 方法。
// 以修改该方法将文档渲染为图像的方式。
auto imageOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// 将 "JpegQuality" 属性设置为 "10"，以在渲染文档时使用更强的压缩。
// 这将减小文档的文件大小，但图像会出现更明显的压缩伪影。
imageOptions->set_JpegQuality(10);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighCompression.jpg", imageOptions);

// 将 "JpegQuality" 属性设置为 "100"，以在渲染文档时使用较弱的压缩。
// 这将提升图像质量，但会导致文件大小增加。
imageOptions->set_JpegQuality(100);
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.JpegQuality.HighQuality.jpg", imageOptions);
```

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
