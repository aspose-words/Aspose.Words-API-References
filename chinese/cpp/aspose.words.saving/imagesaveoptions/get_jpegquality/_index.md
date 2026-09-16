---
title: "Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality 方法"
linktitle: "get_JpegQuality"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality 方法。获取或设置在 C++ 中生成的 JPEG 图像质量的值。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.saving/imagesaveoptions/get_jpegquality/
---
## ImageSaveOptions::get_JpegQuality method


获取或设置决定生成 JPEG 图像质量的值。

```cpp
int32_t Aspose::Words::Saving::ImageSaveOptions::get_JpegQuality()
```

## 备注


仅在保存为 JPEG 时生效。

使用此属性在以 JPEG 格式保存时获取或设置生成图像的质量。该值范围为 0 到 100，其中 0 表示质量最差但压缩率最高，100 表示质量最佳但压缩率最低。

默认值为 95。

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

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
