---
title: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation 方法"
linktitle: "get_UseGdiRasterOperationsEmulation"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation 方法。获取或设置一个值，以确定是否在 C++ 中使用 GDI+ 来模拟光栅操作。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.saving/metafilerenderingoptions/get_usegdirasteroperationsemulation/
---
## MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation method


获取或设置一个值，用于确定是否使用 GDI+ 进行光栅操作仿真。

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_UseGdiRasterOperationsEmulation() const
```

## 备注


可以使用 Windows GDI+ 库来模拟光栅操作。与 Aspose.Words 自己的模拟相比，它提供对所有光栅操作的支持，但在某些情况下性能可能会更慢。

当此值设置为 **true** 时，Aspose.Words 使用 GDI+ 来模拟光栅操作。

当此值设置为 **false** 时，Aspose.Words 使用其自身实现的光栅操作模拟。

此选项仅在元文件被渲染为矢量图形时使用。

默认值为 **false**。

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

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
