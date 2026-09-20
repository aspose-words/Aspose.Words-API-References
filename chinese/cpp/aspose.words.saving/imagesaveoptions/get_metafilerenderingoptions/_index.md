---
title: "Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions 方法"
linktitle: "get_MetafileRenderingOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions 方法。允许在 C++ 中指定在渲染输出时如何处理元文件。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.saving/imagesaveoptions/get_metafilerenderingoptions/
---
## ImageSaveOptions::get_MetafileRenderingOptions method


允许指定在渲染输出中如何处理元文件。

```cpp
System::SharedPtr<Aspose::Words::Saving::MetafileRenderingOptions> Aspose::Words::Saving::ImageSaveOptions::get_MetafileRenderingOptions()
```

## 备注


当指定 [Vector](../../metafilerenderingmode/) 时，Aspose.Words 首先使用其自有的元文件渲染引擎将元文件渲染为矢量图形，然后再将矢量图形渲染为图像。

当指定 [Bitmap](../../metafilerenderingmode/) 时，Aspose.Words 使用 GDI+ 元文件渲染引擎直接将元文件渲染为图像。

GDI+ 元文件渲染引擎速度更快，支持几乎所有元文件特性，但在低分辨率下，与页面上其他矢量图形（尤其是文本）相比，可能会产生不一致的结果。Aspose.Words 元文件渲染引擎即使在低分辨率下也能产生更一致的结果，但速度较慢，且可能对复杂的元文件渲染不准确。

[MetafileRenderingMode](../../metafilerenderingmode/) 的默认值是 [Bitmap](../../metafilerenderingmode/)。

## 示例



展示在将包含 Windows 元文件图像的文档保存为其他图像格式时如何设置渲染模式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertImage(get_ImageDir() + u"Windows MetaFile.wmf");

// 当我们将文档保存为图像时，可以传递一个 SaveOptions 对象给
// 确定保存操作将如何处理文档中的 Windows 元文件。
// 如果我们将 "RenderingMode" 属性设置为 "MetafileRenderingMode.Vector"，
// 或 "MetafileRenderingMode.VectorWithFallback"，我们将把所有元文件渲染为矢量图形。
// 如果我们将 "RenderingMode" 属性设置为 "MetafileRenderingMode.Bitmap"，我们将把所有元文件渲染为位图。
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
options->get_MetafileRenderingOptions()->set_RenderingMode(metafileRenderingMode);
// 当该值设置为 true 时，Aspose.Words 使用 GDI+ 来模拟光栅操作。
options->get_MetafileRenderingOptions()->set_UseGdiRasterOperationsEmulation(true);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.WindowsMetaFile.png", options);
```

## 另见

* Class [MetafileRenderingOptions](../../metafilerenderingoptions/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
